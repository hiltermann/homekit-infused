# Addons for Homekit Infused v3.x

### [Homekit Infused Framework](https://github.com/jimz011/homekit-infused/tree/3.0.0)
### [Homekit Infused Addons Documentation](https://github.com/jimz011/homekit-infused/tree/addons)
### [Homekit Infused All Available Addons](https://github.com/jimz011/homekit-infused/tree/addons/ADDON_LIST.md)

Addons are cards for Homekit Infused. For convenience the addons will be sorted per view as they were intended in previous versions of HKI, however ANY addon you find here can be used on ANY view!


### How to install?
An addon might need additional requirements like a custom card or changes to customize.yaml, you can view requirements at the specific addons page.
Each view has a user section which can be found in the following folder `homekit-infused/user/views/`. To add a card follow the instructions.
Cards that are dropped into this folder will be rendered from top to bottom in alphabetical/numerical order (of the filename).
E.g.
```
In the following folder /homekit-infused/user/views/frontpage/ you have
buttons.yaml
map-card.yaml
weather-card.yaml
```
In this example the buttons will be at the top, below that there will be a map and below that there will be a weather card.

Because the cards will always get rendered in alphabetical/numerical order of the filename you will find that all the addons from this repo will have a double digit in front of the name.
This gives us the opportunity to sort the cards to our likings.

E.g.
```
In the following folder /homekit-infused/user/views/frontpage/ you have
01.weather-card.yaml
02.buttons.yaml
03.map-card.yaml
``` 
In this example you can see that now there is a value and the names all start with the same letter/number. This means the second letter/number takes precedence. So in this example the top card will be a weather card, the second one will be buttons and the third is the map.
You could also do this by naming them `a.weather-card.yaml` and `b.buttons.yaml`. HKI does NOT care about the filename and you can name it whatever you want it to be, it will simply ALWAYS render the cards in alphabetical/numerical order!

You can also add your own files (since HKI doesn't care about the file names, it just cares about the order). 

### Advanced
You can have multiple cards in a single file if you so desire,which might be the case if you want to organise your cards differently or you prefer to have the same type of cards in the same file for easier editing.
When having multiple cards in a file it will still render everything in the same order, so imagine in our previous example that the `weather-card.yaml` file would have two cards (e.g. a simple weather card and a forecast card), it will render the FILES on alphabetical/numerical order, NOT the cards! Remember this!
E.g.
```
In the following folder /homekit-infused/user/views/frontpage/ you have
01.weather-card.yaml (this one has two cards in the file)
02.buttons.yaml
03.map-card.yaml
```
In this example the first card will be the simple weather card, the next one will be a forecast card (so the 2 cards in the first file go first). The third one will be the buttons and the fourth will be the map.
So there are 3 files, but 4 cards (as in the first file there are two cards).

### Get Addons
To view all the available addons and their code [click here](ADDON_LIST.md).
