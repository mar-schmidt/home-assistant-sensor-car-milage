home-assistant-sensor-car-milage
==========================

Car milage per month Sensor component for Home Assistant


Setup
-----
Put the file ``car_milage_per_month.py`` file in the folder ``custom_components/sensor`` of
your local Home Assistant configuration folder ``.homeassistant``.

Your ``configuration.yaml`` file needs an entry for the component including
your cars odometer sensor (``odometer_sensor``).

```yaml
sensor:
  - platform: car_milage_per_month
    odometer_sensor: sensor.ete123_odometer (the sensor that holds the total amount of km)
    scan_interval: 3600
    unit_of_measurement: 'km'
```

Sensor attributes
-------------
The sensor will hold several attributes, one for each month. 
An attribute for the current month is also exposed with the name ``current month`` 
which makes it easy to use in automation (without having to determine the current month yourself).

![alt text](https://github.com/mar-schmidt/home-assistant-sensor-car-milage/blob/master/car_milage_per_month.png)

Extras
-------------
The component will persist the milage data through a file created and located in 
home-assistant home path with filename: milage.json

License
-------
``home-assistant-sensor-car-milage`` is licensed under MIT, for more details check LICENSE.