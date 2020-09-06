# Weather Card
![Homekit Infused](../images/weather-card.png)

### Description
This is a normal weather card simple weather card.

### Requirements (HACS)
| Name | Type  | Description |
|----------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Weather Card](https://github.com/bramkragten/weather-card) | Frontend | This is a customizable animated weather card, see screenshot for details |

### Resources
Add the following line to your lovelace resources 
```/hacsfiles/weather-card/weather-card.js```

### Configuration
To use this you must have dark sky setup, you can follow this page on how to setup darksky.
Below an example of your configuration.yaml:
```
# Example configuration.yaml entry
weather:
  - platform: darksky
    api_key: YOUR_API_KEY
    mode: daily
```
If you want to show the sunrise and sunset times, make sure the sun component is enabled:
```
# Example configuration.yaml entry
sun:
```

### Advanced
| Parameters | Type | Default | Description |
|----------------------------------|-------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| entity | String | weather.dark_sky | Sets the weather entity used for this card |
| current | Boolean | true | Show the current weather icon, the current temperature and title |
| forecast | Boolean | true | Shows forecast |
| hourly_forecast | Boolean | False | Shows hourly forecast |
| number_of_forecasts | Integer | 5 | Shows number of forecasts |


### Install
- Create a new file inside the folder of the view you want (e.g. /homekit-infused/user/views/frontpage/), you can name the file however you want (e.g. weather-card.yaml)
- Copy the code below and make changes if needed

```
- type: horizontal-stack
  cards:
    - !include ../../../base/includes/gap.yaml
    - type: custom:weather-card
      style: |
        ha-card {
          font-size: 12px;
          font-family: Helvetica;
          border-radius: var(--border-radius);
          box-shadow: var(--box-shadow);
          opacity: 0.8;
        }
      entity: weather.dark_sky
      current: true
      details: true
      forecast: true
      hourly_forecast: false
      number_of_forecasts: 5
    - !include ../../../base/includes/gap.yaml
```

