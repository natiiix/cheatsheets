# Raspberry Pi

## wpa_supplicant.conf

You may want to replace the country code with your country code. A handy list of the two-letter country codes can be found [here on Wikipedia](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2).

```
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
country=US
update_config=1

network={
    ssid="<SSID>"
    psk="<password>"
    key_mgmt=WPA-PSK
}
```
