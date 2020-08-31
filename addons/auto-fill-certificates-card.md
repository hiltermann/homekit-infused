# Auto Filled Certificates Card (show expiry dates)
![Homekit Infused](../images/certificates-card.png)


### Requirements (HACS)
| Name | Type  | Description |
|----------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NONE] | None | Not applicable |

### Configuration
- No configuration required (experienced users can change the style if they wish)

### Install
- Create a new file in the view you want (e.g. /homekit-infused/user/views/certificates/), you can name it however you want
- Copy the code below and make the necessary changes

```
- type: horizontal-stack
  cards:
    - !include ../../../base/includes/gap.yaml
    - type: custom:auto-entities
      filter:
        exclude:
          - entity_id: '*timestamp*'
        include:
          - entity_id: 'sensor.cert_expiry_*'
      show_empty: false
      sort:
        method: name
        numeric: true
      card:
        type: entities
        style: |
          ha-card {
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
          }
        columns: 3
    - !include ../../../base/includes/gap.yaml
    ```
