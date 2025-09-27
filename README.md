# ULK

Low profile split keyboard with Corne 42 Layout and Cherry ULP switches. Made to be used on top of a laptop keyboard to provide the ultimate split experience on the go. 

Due to the availability of the ULP switches only the Click version was available which is nice for home, however too loud for work at public places.

## Contents
   - [Disclamer](#Disclamer)
   - [Curent Issues](#Issues)
   - [Things to do](#Things-to-do)
   - [Gallery](#Gallery)
   - [BOM](#BOM)
   - [Firmware](#Firmware)
## Disclamer

This Design is still under development and has [Issues](#Issues)!

## Issues: 
   Current Issues:
   - Hole attachment point interferes with USB-C charging cables. (These also truned out to be not needed so they will be removed)
   - Battery connection should be changed form a through hole to SMD, so there are no chances of shorting a battery when putting keyboard on

## Things to do: 
   - Solder up the proper batteries.
   - Add support for solar charging.
   - Build a version with 35g PG1316s.
   - Change the reset button to a lower profile SMD version.


## Gallery
![169full](https://github.com/user-attachments/assets/05deb97c-3cea-4f9b-9afd-9c0f920b93a3)
![169su](https://github.com/user-attachments/assets/6171a4a0-babd-41de-bf22-33484fe64383)
![169pcb](https://github.com/user-attachments/assets/975600b9-8b46-49eb-9b58-9a906919e12c)
<img width="3246" height="1263" alt="ULK v7" src="https://github.com/user-attachments/assets/6b71d21b-0977-4e59-85f4-adc084f5ee60" />
<img width="3643" height="2032" alt="ULK_frontr" src="https://github.com/user-attachments/assets/8aa226fc-b96f-4503-b2aa-d7c64b0e6250" />
<img width="3643" height="2032" alt="ULK_backr" src="https://github.com/user-attachments/assets/8787084f-663e-4d1d-9f8e-910db36c4c64" />
![PXL_20250926_071452410 MP](https://github.com/user-attachments/assets/29f99179-fd28-4f6c-8c52-36672acb1f1b)


# BOM

## Main Components

| Name             | Specification                                                                 | Notes                                             |
|------------------|-------------------------------------------------------------------------------|---------------------------------------------------|
| Switches         | Cherry ULP or Kailh PG1316S                                                   | —                                                 |
| Keycaps          | 1U Kailh PG1316S Keycaps                                                      | —                                                 |
| Diodes           | 1N4148W in SOD-123 package                                                    | —                                                 |
| Microcontroller  | SuperMini NRF52840                                                            | Compatible with nice!nano V2 and alternatives ([GitHub link](https://github.com/joric/nrfmicro/wiki/Alternatives)) |
| Power switch     | 7Pin Mini Slide Switch                                                        | —                                                 |
| Reset button     | 3x6x4.3mm push button                                                         | Will to an smd one after testing samples          |
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

## Firmware 

You can use the standart Conre ZMK firmware.

I use a modified verion of the MC Technology's zmk-config [GitHub link](https://github.com/Goga64/zmk-config-ULK).
My version also allows for 4 halfs of a spit be connected with to one Dongle at the same time.





