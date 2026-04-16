# ULK

Low profile split keyboard with Corne 42 Layout and Cherry ULP switches. Made to be used on top of a laptop keyboard to provide the ultimate split experience on the go. 

## Contents
   - [Description](#Description)
   - [Gallery](#Gallery)
   - [BOM](#BOM)
   - [Firmware](#Firmware)
   - [Inspirations](#Inspirations)
     
![169full](https://github.com/user-attachments/assets/05deb97c-3cea-4f9b-9afd-9c0f920b93a3)
![Gallery/ulk_sl_left_crop.jpg](https://github.com/Goga64/ULK/blob/953767bf9aa2bdcd04b6005427a60ab565788cff/Gallery/ulk_sl_left_crop.jpg)



# Description

## Switches
### Sound  
I have recorded some [samples](https://github.com/Goga64/ULK/tree/e7978e2b8ab778f136db2aed6a6b6116afc4dded/Sound). For all of them the keyboard was on a mousepad.

I prefer the sound of the ULP Click, although it is still not as nice as the full size switches.

### Feel
The Cherry ULP feel quite satifying to type on, however they are a bit heavy coming in at 65g. The PG1316s though I'm not as impressed by, I got the 35g version which is very light, it makes the typing feel effortless, it doesn't really feel like anything. With it I also struggle with typos while writing as extra letters will just appear out of nowhere. It is definetry something I need to get used to before I can give a better oppinion. I will probably want to try the 60g version of them in the future and if they made a 50g version I would build another keeb with them immediately.  

## Solar

## Firmware
The non-solar versions use standard Conre ZMK firmware.


The solar version however is diodeless, thus it is direct wired. So you should use my a modified verion of the MC Technology's zmk-config [GitHub link](https://github.com/Goga64/zmk-config-ULK)


The firmware was one of the biggest roadblock in getting the whole thing working. As it has 21 keys per side it uses all of the GPIO avaliable on a ProMicro including three marked purple here:

<img width="200"  alt="Screenshot 2026-04-16 212617" src="https://github.com/user-attachments/assets/b57fe391-57f5-422f-8a0e-bd552aa073c7" />


As they are not included in the original pinout on the main ZMK branch I needed fork and change the [pinout](https://github.com/Goga64/zmk/blob/v0.3-branch/app/boards/arm/nice_nano/arduino_pro_micro_pins.dtsi) to include them. 


I have also not wired up both sides as a mirror of each other on the PCB which has lead to a weird [keymap_transform](https://github.com/Goga64/zmk-config-ULK/blob/7f940e578cdd5d7742a9fed1b120f3a784b748a8/boards/shields/ulk_sl/ulk_sl.dtsi).




## Things to do: 
   - Add a 3x5 option.
   - Update BOM for sl version
   - Solar writeup


## Gallery
More images can be found in the [Gallery folder](https://github.com/Goga64/ULK/tree/953767bf9aa2bdcd04b6005427a60ab565788cff/Gallery).
They were taken on a Cannon EOS5D mkii (2008) and an EF 24-70mm F/2.8 USM lens.


I had a lot of fun focus stacking them for the best sharpness.


# BOM

## Main Components

| Name             | Specification                                                                 | Notes                                             |
|------------------|-------------------------------------------------------------------------------|---------------------------------------------------|
| Switches         | Cherry ULP or Kailh PG1316S                                                   | You can find more about the ULP at [Cherry_MX_ULP](https://github.com/pashutk/Cherry_MX_ULP)                                                |
| Keycaps          | 1U Kailh PG1316S Keycaps                                                      | —                                                 |
| Diodes           | 1N4148W in SOD-123 package                                                    | —                                                 |
| Microcontroller  | SuperMini NRF52840                                                            | Compatible with nice!nano V2 and alternatives ([GitHub link](https://github.com/joric/nrfmicro/wiki/Alternatives)) |
| Power switch     | 7Pin Mini Slide Switch                                                        | —                                                 |
| Reset button     | 3x6x4.3mm push button                                                         | Will change to an smd one after testing samples   |
| Battery          | ~100mAh 401525 LiPo or smaller                                                | Prototype photos show 750mAh HiV battery due to shipping delays |

## Optional Components

| Name        | Specification                                       | Notes                                             |
|-------------|---------------------------------------------------|---------------------------------------------------|
| Non-slip    | 1 mm Silicone Rubber Strip, Self Adhesive           | Increases overall thickness to 6.8mm              |
| Kapton tape | Polyimide insulating tape                           | To cover through-hole components on bottom of PCB |


<!---
## BOM
Switches - Cherry ULP or Khali PG1316S
Keycaps - 1U Kailh PG1316S Keycaps 
Diodes - 1N4148W in SOD-123 package
Microcontroller - SuperMini NRF52840 - compatable with nice!nano V2 and it's alternatives https://github.com/joric/nrfmicro/wiki/Alternatives
Power switch - 7Pin Mini Slide Switch
Reset button -  3x6x4.3mm push button - Will probably be changed, when I get a sample of buttons.
Battery - ~100mAh 401525 Lipo or smaller - On the pictures a 750 mAh HiV battery is used due to battery shipping taking a long time and I had those lying around.

Optional
Non-slip - 1 mm Silicone Rubber Strip Self Adhesive (thinkness increases to 6.8mm).
Capton tape - to cover the through hole components on the bottom side of the pcb.
-->

## Inspirations
- [foostan/crkbd](https://github.com/foostan/crkbd)
- [mctechnology17/zmk-config](https://github.com/mctechnology17/zmk-config)
- [pashutk/Cherry_MX_ULP](https://github.com/pashutk/Cherry_MX_ULP)
- [zmk-config-mikefive](https://github.com/mikeholscher/zmk-config-mikefive)
- [ZMK](https://zmk.dev/)


