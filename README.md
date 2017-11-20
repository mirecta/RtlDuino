# RtlDuino
Arduino module RTL00(RTL8710AF), [F11AMIM13](http://fn-link.en.made-in-china.com/product/sSinPtAKZBke/China-RTL8711AM-Iot-Module.html) (RTL8711AM), [F11AFIM13-B1](http://fn-link.en.made-in-china.com/product/PSHnuEtJVXWh/China-RTL8711AF-IoT-Module-IEEE-802-11-B-G-N-2-4GHz-1T1R-WiFi-NFC-Module.html) (RTL8711AF)<br>
[PADI](https://www.pine64.org/?page_id=946) (RTL8710AF), [F10AFIM13-B1](http://en.ofeixin.com/products_detail/productId=65.html) (RTL8710AF), [TinyCon2005-A-BE](http://www.ralinwi.com/product.aspx?info_lb=54&flag=1) (RTL8711AF),<br>
[WFM-400](http://www.rayson.com/rayson/en/?pros=product&pros=product&b_cat_id=A03&m_cat_id=A0304&s_cat_id=A030401&prod_id=P0113&level=3) (RTL8711AM), [WFM-410](http://www.rayson.com/rayson/en/?pros=product&pros=product&b_cat_id=A03&m_cat_id=A0304&s_cat_id=A030401&prod_id=P0114&level=3) (RTL8711AF), [WFM-250](http://www.rayson.com/rayson/en/?pros=product&pros=product&b_cat_id=A03&m_cat_id=A0304&s_cat_id=A030401&prod_id=P0112&level=3) (RTL8195AM),<br>
[AW-CU238, AW-CU239](https://www.buyiot.net/pd-1) (RTL8711AM), [AW-CU245, AW-CU245, AW-CU245](https://www.buyiot.net/home-1) (RTL8711AM/RTL8195AM/RTL8711AF),<br>
[WG6611](http://www.jorjin.com/product.php?id=98) (RTL8711AM), [RAK473](http://www.rakwireless.com/en/download/RAK473/Firmware%20Upgrade) (RTL8711AM), [RAK474, RAK476](http://www.rakwireless.com/en/download/RAK473/Firmware%20Upgrade) (RTL8711AF),
[6110R-IF](http://en.ofeixin.com/products_detail/productId=65.html) (RTL8710AF),<br>
[MJIOT-AMB-01](http://www.nb-iot-tech.com/mjiot-amb-01-en.html) (RTL8710AF), [MJIOT-AMB-02](http://www.nb-iot-tech.com/mjiot-amb-02-en.html) (RTL8195AM), ...<br>

### Development Status

List of improvements/differences to https://github.com/pvvx/RtlDuino
* Arduino **String** support binary data
* Basic support RTL Cryptographics API (only MD5 at this time)
* Ported HTTP server from ESP8266  https://github.com/esp8266/ESPWebServer
  * Http auth uses hw MD5 calculation
  * Server can receive and send binary data (application/octet-stream) for optimalization (more work can do in javascript client side) (original server not support this)
  * Server has new method for serving static from documentroot from SD card
  * In sending file try to find gz version and automatic choose this variant for minimalisation of data transfer
* Some fixes Wifi library for new webserver
* Improvement SDFat , u can open file with modes r,r+,w,w+,a,a+ (for write for append etc.)
* Add option to flash RTL8710 via stlink and openocd (u must install openocd)



### Installation
- Install Arduino IDE and Ameba (reference: http://www.amebaiot.com/ameba-arduino-getting-started/ )
- Go to Arduino IDE installation directory
- Clone this repository into hardware/development/rtl87xx directory (or clone it elsewhere and create a symlink)
- Restart Arduino

### Pins RTL00
![SCH](https://github.com/pvvx/RtlDuino/blob/master/ArduinoRTL00.gif)

### SD cards
![SCH](https://github.com/pvvx/RtlDuino/blob/master/SD_card.gif)


(More info: https://esp8266.ru/forum/threads/arduino-dlja-rtl8710.1787/ )
