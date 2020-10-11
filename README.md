# HomeAssistant---WyzeSensorAttributes

Dependancies:

https://github.com/kevinvincent/ha-wyzesense awesome work !!

From HACS > Frontend Add 'custom:multiple-entity-row' to "...show multiple entity states, attributes and icons on entity rows in Home Assistant's Lovelace UI.."
This is not a standalone lovelace card, but a row element for the entities card.

Great example for all use cases: https://awesomeopensource.com/project/benct/lovelace-multiple-entity-row?categoryPage=4



From the Lovelace UI, add 'Entities' card, then select to 'Edit' the card, select 'Visual Editor' and paste in and save. 

You may get errors from UI as it cannot handle all object attributes, just make sure yaml formatting is good, UI will highlight those errors.


  - entity: binary_sensor.wyzesense_motion_garage
  # replace binary_sensor.wyzesense_motion_garage with your entity device name
    type: 'custom:multiple-entity-row'
    name: Wyze Motion Sensor - Garage
  # replace name with something that works for you
    show_state: false
  # hides the entity status, not needed for me
    entities:
  # find the attributes of your entity in HA under Developer Tools then select requried entity to list
      - attribute: battery_level
        name: Battery
        unit: '%'
      - attribute: rssi
        name: Network
