# Locate My Device
This app helps to locate a lost smartphone through the use of conventional SMS. **It is in beta and under active development**

## Screenshots
| Homescreen | SMS Chat
|:-:|:-:|
| <img src="/images/home.png" alt="Homescreen" width="190" height="390.641"> | <img src="/images/sms.png" width="190" height="390.641"> |

## Usage
Send an SMS to the device you want to locate in order to retrieve information about it.

**Synopsis**
<br/>
```activation_command password option```

**Default values**
<br/>
* The default value for ```activation_command``` is ```LMD```
* The default value for ```password``` is ```0000```. It's highly encouraged to change it

**Options**
Option | Explaination | Required permission
-------|:------------|--------------------|
locate | Will return the most accurate set of coordinates possible and a link to them pinpointed to OpenStreetMap | Location
cellinfo | Will return a set of uniquely identifiable information about cell towers near the phone. You can then put this information on [OpenCellId][1] to individuate the smartphone's approximate location | Location
battery | Will return battery infos | None |
lock | Will  lock down the smartphone | Device Administrator |
show "message" | Will show a message on the screen, even when it's locked. | Overlay |
callme | You will receive a call from the lost smartphone | Calls, Overlay |
wifi | Will return Wi-Fi infos | Location |
wifi-enable | Will enable Wi-Fi (Only API < 29) | None |
wifi-disable | Will disable Wi-Fi (Only API < 29) | None |

## Legal notice
* This software is licensed under the GNU General Public License v3.0. Click [here](https://github.com/xfarrow/locatemydevice/blob/main/LICENSE) for more information;
* As specified in the license, the software is provided "as is" with no warranty;
* This software is not meant to be the only installed device locator. It is strongly advised to use it in conjunction with Google Find My Device; in fact it might suffer from a bug or might be unresponsive when you need it the most;
* The logo has been provided to  me for free by [Iconfinder](https://www.iconfinder.com/)

## Why?
There is already Google Find My Device, but I wanted to develop a free and open source alternative (even tho it is suggested to keep Google's, unless you do not have Play Services and/or wanting to go full-in about privacy). There is already a good FOSS alternative, [Find My Device](https://gitlab.com/Nulide/findmydevice), but wanted to change it a little. I did [fork](https://www.github.com/xfarrow/FindMyDevice) it, but eventually decided to create my own project.

## Beware of malwares
GitHub's releases page is the only place where I am uploading apks.

## Support
If you enjoy this software, a little star is highly appreciated: it shows me people enjoy it.

You can also donate if you want to, using the button below

<noscript><a href="https://liberapay.com/xfarrow/donate"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a></noscript>

[1]: https://opencellid.org/
