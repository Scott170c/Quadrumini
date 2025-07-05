# Quadrumini
### Affordable quadruped robot that can be modded with basic functionality! Updated models [HERE](https://github.com/Scott170c/Quadrumini/tree/main/inDev/QuadruminiV3)
```
Goals:
- Under $65 USD per unit
- Easy to assemble (be made into a kit?)
- Easy to modify
```
## Current Version: ` 3 `
<br></br>
<img src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/6856774ca16c4dd138cb67b755833bc600993292_image.png" height="500px">

Why I made this: <br>
After watching Boston Dynamics, I was always interested in quadrupedal robots (spot) and legged robots. I have seen many different quadrupedal robots both big and small, but a common factor between them is that they are all expensive. I wanted to make my own affordable (but high quality) version at home so I could learn how they worked and enjoy having one :)
<br></br>
<img src="https://hc-cdn.hel1.your-objectstorage.com/s/v3/e8d69d5ab9a51e5d848373264149c8728fc938db_image.png" height="500px">

BOM:
|Component        |Description                          |Cost (USD)|Notes                                                        |Link                                                                                                                                                        |
|-----------------|-------------------------------------|----------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
|MG90S Servos     |Small metal gear servo motor         |29.99     |most cost efficient motor to use that wont snap when using   |https://www.amazon.com/MG90S-Servo-Motor-Helicopter-Arduino/dp/B0CNL7Z2VY                                                                                   |
|Raspberry Pi Pico|Microcontroller                      |3.99      |For controlling the robot                                    |https://www.microcenter.com/product/661033/raspberry-pi-pico-microcontroller-development-board                                                              |
|2S Lipo Battery  |Lipo Battery 1000mah                 |8.99      |Lightweight, around 60g                                      |https://www.amazon.com/Gens-ace-1000mAh-Helicopter-Airplane/dp/B012CMFAL2/ref=sr_1_2_sspa?s=toys-and-games&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1|
|UBEC             |Universial Battery Eliminator Circuit|3.15      |to step down voltage to safe operating voltage for components|https://www.aliexpress.us/item/2255799846479441.html?spm=a2g0o.productlist.main.10.270158PP58PPCb&algo_pvid=d286b7fc-346a-4e5d-9749-a3a6a5d45b98&algo_exp_id=d286b7fc-346a-4e5d-9749-a3a6a5d45b98-9&pdp_ext_f=%7B%22order%22%3A%2271%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%213.15%213.15%21%21%213.15%213.15%21%402101e07217514034438407783eafc7%2110000000073941053%21sea%21US%214343322020%21X&curPageLogUid=HjvgqpsAf3u7&utparam-url=scene%3Asearch%7Cquery_from%3A|
|PCB              |For driving the the motors, computing|80.79     |not needed for now, will prob use stray components           |LCSC                                                                                                                                                        |
|MPU6050          |for Gyro/Accel                       |1.86      |Not needed, can be added for extra sensing                   |https://www.aliexpress.us/item/3256809057355938.html?spm=a2g0o.productlist.main.1.41395c1dFMOhrF&algo_pvid=fd1f46ea-ccf6-4eba-a5c4-611fbd8cb636&algo_exp_id=fd1f46ea-ccf6-4eba-a5c4-611fbd8cb636-0&pdp_ext_f=%7B%22order%22%3A%2220%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%215.02%211.86%21%21%2135.73%2113.22%21%402101ec1a17514039581717786ec293%2112000048448136985%21sea%21US%214343322020%21X&curPageLogUid=B2b3K1XhIUKY&utparam-url=scene%3Asearch%7Cquery_from%3A|
Total: | $126.91 USD |

Handwire (I will be following this):
|Component            |Description                                 |Cost (USD)|Notes                                           |Link       |
|---------------------|--------------------------------------------|----------|------------------------------------------------|-----------|
|MG90S Servos         |Small MG (metal gear) servo                 |$29.99    |Smallest motor w/ metal gears for added strength|https://www.amazon.com/MG90S-Servo-Motor-Helicopter-Arduino/dp/B0CNL7Z2VY|
|Raspberry Pi Pico    |MCU to control the robot (the brain)        |$3.99     |For controlling the robot                       |https://www.microcenter.com/product/661033/raspberry-pi-pico-microcontroller-development-board|
|2S Lipo Battery      |Lipo Battery (1000 mah , 7V)                |$8.99     |Lightweight, around 60g                         |https://www.amazon.com/Gens-ace-1000mAh-Helicopter-Airplane/dp/B012CMFAL2/ref=sr_1_2_sspa?s=toys-and-games&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1|
|UBEC                 |Battery eliminator circuit                  |$3.15     |Needed to step down voltage from 7V to 5V       |https://www.aliexpress.us/item/2255799846479441.html?spm=a2g0o.productlist.main.10.270158PP58PPCb&algo_pvid=d286b7fc-346a-4e5d-9749-a3a6a5d45b98&algo_exp_id=d286b7fc-346a-4e5d-9749-a3a6a5d45b98-9&pdp_ext_f=%7B%22order%22%3A%2271%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%213.15%213.15%21%21%213.15%213.15%21%402101e07217514034438407783eafc7%2110000000073941053%21sea%21US%214343322020%21X&curPageLogUid=HjvgqpsAf3u7&utparam-url=scene%3Asearch%7Cquery_from%3A|
|PCA9685 Servo Driver |Drives servos through I2C                   |$3.34     |Needed to drive all of the servos               |https://www.aliexpress.us/item/3256808284749606.html?spm=a2g0o.productlist.main.1.7aa461f02vdrHM&algo_pvid=510162e8-403b-4996-9b8d-2b3981fe036d&algo_exp_id=510162e8-403b-4996-9b8d-2b3981fe036d-0&pdp_ext_f=%7B%22order%22%3A%22266%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%217.75%213.34%21%21%2155.13%2123.71%21%402103146f17514042330173497e7ff2%2112000045292167540%21sea%21US%214343322020%21X&curPageLogUid=oBqDMpUY0xVr&utparam-url=scene%3Asearch%7Cquery_from%3A|
|MPU6050              |For sensing Gyro/Accel                      |$1.86     |Not needed, can be added for extra functionality|https://www.aliexpress.us/item/3256809057355938.html?spm=a2g0o.productlist.main.1.41395c1dFMOhrF&algo_pvid=fd1f46ea-ccf6-4eba-a5c4-611fbd8cb636&algo_exp_id=fd1f46ea-ccf6-4eba-a5c4-611fbd8cb636-0&pdp_ext_f=%7B%22order%22%3A%2220%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%215.02%211.86%21%21%2135.73%2113.22%21%402101ec1a17514039581717786ec293%2112000048448136985%21sea%21US%214343322020%21X&curPageLogUid=B2b3K1XhIUKY&utparam-url=scene%3Asearch%7Cquery_from%3A|
|Logic-Level Converter|shifting logic from 5V to 3V3 for PCA module|$2.41     |Needed to shift to lower voltage logic          |https://www.aliexpress.us/item/3256808042987546.html?spm=a2g0o.productlist.main.2.62304c42H9SNtD&algo_pvid=e68dff8b-8817-408e-8a2f-c78135c1fbbb&algo_exp_id=e68dff8b-8817-408e-8a2f-c78135c1fbbb-1&pdp_ext_f=%7B%22order%22%3A%22832%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%216.71%212.41%21%21%2147.76%2117.19%21%402101c59117514043270215311e0255%2112000044305257486%21sea%21US%214343322020%21X&curPageLogUid=QqzTP1nuaS8c&utparam-url=scene%3Asearch%7Cquery_from%3A|
Total: | $53.73 USD |
