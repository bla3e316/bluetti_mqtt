# Bluetti to MQTT

MQTT bridge between a Bluetti power station and Home Assistant.

Leave the MQTT host, port, username, and password empty when the Mosquitto add-on is installed. Set `bt_mac` to the station's Bluetooth address. Use `mode: mqtt` for normal operation.

`discovery` and `logger` write files under `/share/bluetti2mqtt` and do not publish MQTT messages.
