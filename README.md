# pan-tilt-phat-HASS
This component adds the [pimoroni](https://shop.pimoroni.com/products/pan-tilt-hat) pan-tilt-phat to [Home-assistant](https://home-assistant.io/).

* Test you camera.
* Place the pan_tilt_phat.py file in your custom components folder, i.e. <config_dir>/custom_components/sensor/pan_tilt.py
* Add to your configuration file:

```
script: !include scripts.yaml

camera:
  - platform: rpi_camera
    vertical_flip: 1

sensor:
  platform: pan_tilt_phat

group:
  default_view:
    view: yes
    icon: mdi:home
    entities:
      - camera.raspberry_pi_camera
      - group.controls_group

  controls_group:
    name: Controls
    entities:
      - sensor.pan_tilt_phat
      - script.1503899567501
```

<img src="https://github.com/robmarkcole/pan-tilt-phat-HASS/blob/master/my_pan_tilt.png">
<img src="https://github.com/robmarkcole/pan-tilt-phat-HASS/blob/master/main_hass_pan_tilt.png">
<img src="https://github.com/robmarkcole/pan-tilt-phat-HASS/blob/master/call_pan_tilt.png">
