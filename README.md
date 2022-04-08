# IoTwin | Data Generator

[![Python](https://badgen.net/pypi/python/black)](https://www.python.org/downloads/)
[![Linux](https://svgshare.com/i/Zhy.svg)](https://svgshare.com/i/Zhy.svg)
[![CodeQL](https://github.com/CTISenior/iot-device-simulator/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/CTISenior/iot-device-simulator/actions/workflows/codeql-analysis.yml)
[![linting: pylint](https://img.shields.io/badge/linting-pylint-yellowgreen)](https://github.com/PyCQA/pylint)

> It is developed and designed for developers. (Tested on Ubuntu 20.04)

## Installation

```
>_ sudo apt update -y
>_ sudo apt install -y python3-dev python3-pip git libglib2.0-dev libxkbcommon-x11-0 libqt5x11extras5
>_ git clone https://github.com/CTISenior/iotwin-data-generator.git
>_ cd iotwin-data-generator
>_ sudo python3 setup.py install
>_ sudo python3 ./iotwin_data_generator/main.py
```


### default "config/settings.json" file

```
{
    "gateway": {
        "name": "Test Broker",
        "client_id" : "test_id",
        "host": "127.0.0.1",
        "default_keys": ["temp", "hum", "custom"],
        "security": {
            "isSecure": false,
            "username": "username",
            "password": "password"
        },
        "ssl": {
            "certificates": false,
            "cert": "~/ssl/cert.pem",
            "key": "~/ssl/key.pem"
        },
        "protocols": {
            "mqtt": {
                "name": "mqtt",
                "port": 1883,
                "topic_name": "/sensor/data",
                "method": null,
                "telemetry_keys":["serialNumber", "deviceName", "deviceType"],
                "security": {
                    "isSecure": false,
                    "username": "username",
                    "password": "password"
                },
                "ssl": {
                    "certificates": false,
                    "cert": "~/ssl/cert.pem",
                    "key": "~/ssl/key.pem"
                }
            },
            "http": {
                "name": "http",
                "port": 5000,
                "topic_name": "/device",
                "method": "post",
                "telemetry_keys":["serialNumber", "sensorName", "deviceType"],
                "security": {
                    "isSecure": false,
                    "username": "username",
                    "password": "password"
                },
                "ssl": {
                    "certificates": false,
                    "cert": "~/ssl/cert.pem",
                    "key": "~/ssl/key.pem"
                }
            },
            "": {

            }
        }
    }
}
```

### default "data/devices.json" file

```
{
    "devices": [
 
    ]
}
```