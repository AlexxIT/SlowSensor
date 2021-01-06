# Slow Sensor

Home Assistant component to demonstrate problem freezing whole Hass from only one "bad" component. 

## Configuration

Every 5 seconds your Hass will not show signs of life for 5 seconds:

```yaml
sensor:
  - platform: slow_sensor
    scan_interval: '00:00:05'
    sleep: 5
```

Similar example, but you won't get **WARNING**:

    Updating slow_sensor sensor took longer than the scheduled update interval 0:00:05

```yaml
sensor:
  - platform: slow_sensor
    scan_interval: '00:00:10'
    sleep: 5
```