# Overview 
The supply scheme chosen was as follows: 
* USB C port 
* Linear battery charger
* Linear regulator with slide switch on the input side 

## USB Port 
The USB port would allow for data transfer to the ESP32 as well as charging of the battery.

## Linear Charger
The linear charger would charge the battery whilst simultaneously providing sufficient power to run all down stream devices

## Linear Regulator
The power budget for the system included the following: 

| Device        | Manufacturer Spec                                                                                                                                            | Current (mA) |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| ESP32-WROOM-2 | [[esp32-s3-wroom-2_datasheet_en.pdf#page=29&selection=89,0,90,1&color=yellow\|0.5]]A                                                                         | 500          |
| STM32C0       | [[stm32c011f6.pdf#page=39&selection=90,0,91,0&color=yellow\|3.05]]mA @48MHz<br>[[stm32c011f6.pdf#page=39&selection=210,5,210,6&color=yellow\|0.150]]mA @1MHz | 3            |
| LCD Backlight | [[ER-TFT035IPS-6_Datasheet.pdf#page=11&selection=211,0,211,3&color=yellow\|120]]mA                                                                           | 120          |
|               |                                                                                                                                                              |              |

Therefore a 1A linear regulator was selected to comply with the minimum requirements set out by the device manufacturers. 