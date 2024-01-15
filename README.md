# mobiflight-configs
My configurations for mobiflight

## A20N
was created for the FlyByWire A32nx Airbus A320neo (A20N).

## GENERIC_AP-V6_ASOBO_PLANES
![Overview of Gerneric AP Config]("img/GENERIC_AP-V6_ASOBO_PLANES OVERVIEW.jpg")
was taken from [https://flightsim.to/file/67143/generic-ap-asobo-planes-minicockpit-minifcu-mobiflight-profile-full-installation](https://flightsim.to/file/67143/generic-ap-asobo-planes-minicockpit-minifcu-mobiflight-profile-full-installation).

My MobiFlight config file to support the miniFCU with Displays on generic Asobo Planes (C172 G1000....)
(Inclusive full instructions with a new unit)

FIRST TIME INSTALLATION INSTRUCTIONS:
1. Ensure your miniFCU is fully regristered as USB-SERIAL CH340 in your windows device manager, otherwise check here: https://shop.minicockpit.com/a/help/article/57597
   => if it won´t after driver installation or windows update you may use another or the original USB cable (power+data transport cable required!)
2. Close the miniFCU DLS (data link software), it´s not needed and causes issues if used together with Mobiflight
3. Download & install latest MobiFlight version, then upgrade to latest beta (see below) https://www.mobiflight.com/en/download.html
   => Extras => Settings: UNTICK! "Automatically perform retrigger-action with "run" mode (otherwise all buttons will be pressed if you run MF)
   ![SettingRetriggerOnRun]("img/NOTE - SettingRetriggerOnRun.gif")
   => Extras => Settings: TICK "yes, i would like to receive beta version updates", then "OK" (actually it works only with MF Beta)
   => Upgrade to latest Beta & restart Mobiflight
   => If not already done, ensure you installed the Mobiflight WASM module => Extras => MSFS2020 => Install WASM module 
   => check in your MSFS community, you have got a "mobiflight-event-module" folder, otherwhise its installed on the false location and won´t work
4. With a original or older miniFCU device, Mobiflight will now upgrade your firmware (do it) that it´s useable with Mobiflight
   => go though firmware updating messages, then in configured modules => right mouse click on "compatible" => "update firmware" => "minicockpit" => "miniCOCKPIT miniFCU"
   ![UpdateFirmware]("img/NOTE - UpdateFirmware.gif")
5. Then "Upload" the boards default config (below the miniFCU picture) and click "OK"
   => Note you can restore the Firmware anytime same way: right mouse click on miniFCU (configured modules) => "Reset board" to get it usage with miniFCU DLS

**CONFIG INTEGRATION:**
Now all is prepared and the next steps must be done everytime you upgrade a config

   6. Download & Extract my GENERIC_AP-V6_ASOBO_PLANES.zip
   7. Open the config (.mcc) in Mobiflight (File -> Open -> select it)
   8. Important or you won´t get Display values later:
   => Orphaned Serials found window opens => in the white field select my "miniCOCKPIT miniFCU/ SN-94G-809" serial that its blue marked -> "Assign"
   => then my serial will disappear and the config is adjusted to your serial => click "OK" => "Save" (otherwise you have to do it every time)
![AssignBoardToConfig]("img/NOTE - AssignBoardToConfig.gif")
- Optional but recommended, on Mobiflight bottom right mouse click on your selected aircraft => link current config & "Auto load linked config"
-  Optional but recommended; on Mobiflight top, activate "AutoRun" (yellow pulp if activated)
Now you are ready to use and enjoy


HANDLING / USAGE NOTES & INFORMATIONS:
- Don´t worry about the red "!" circles if config is running, these are programmed preconditions (logic) and normal
- Display values will appear earliest if sitting in the plane and MF config is on "RUN" (running)
  Best to get it working is the following way (otherwhise it may not get synced)
1) start msfs and stay in the main menu
2) start mobiflight
3) select your plane
4) click MF and run the config (if not already)
5) start your flight & enjoy

Cheers, vinKaiZen

MiniCockpit Community Discord: https://discord.gg/63ypEhYkft
Mobiflight Discord: https://discord.gg/QjCQXSQs5K

Don´t miss the Fenix A320 Config
https://de.flightsim.to/file/67139/fenix-a320-minicockpit-minifcu-mobiflight-profile-quartz-displays-full-installation


###CHANGELOG V6 
*(Config is for MF 10.0.2.3 with miniFCU Firmware 0.9.3)*
- changed all LED output logic to 0.9.3 Firmware

### CHANGELOG V5
- fixed 100/1000 output
- added added layer switch via HDG<>TRK button (spd encoder & value = crs1, hdg encoder & value = crs 2)
- moved AP FLC (flight control change) from spd encoder pull to EXPED button
- fixed AP2 LED (without function, state was on)

### CHANGELOG V4
- ALTINC with 100/1000ft for AP is now working

CHANGELOG V1-3
- initial config build

## H135
has been built for the Hype Performance Group HPG Airbus Helicopters H135 (H135) freeware helicopter.

## K100
has been built for the SWS Kodiak 100 (K100) payware aircraft.

## VL-3
is for the Asobo VL-3 Evolution Ultralight Aircraft
