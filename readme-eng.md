<p align="right"><a href="https://github.com/YakkaDev/CS-GO-Crosshair-Manager"><sup>RU</sup></a></p>


# CS:GO Crosshair Manager

**Crosshair Manager** is a tool for organizing, interacting and managing your crosshairs, their settings and dependencies from a single configuration file.

<p align="center"><img src="/images/preview.gif"> </p>

This organizer provides the ability to use several presets for your sights at the same time. Each preset contains the configuration of the smoke sight, primary and secondary slots. Summary: Crosshair Manager is a tool that allows you to hot-swap up to four different sights with a single keystroke and directly during a match.

Now all your configurations are much easier to store. It is no longer necessary to edit autoexec.cfg each time, because each crosshair is stored and read from its own file, and all settings are available in `crosshair-UI.cfg`.

---

## Install

To install the manager, you need to transfer all files from [archive](https://github.com/YakkaDev/CS-GO-Crosshair-Manager/releases/download/v1.1/Crosshair-M.v1.1.rar) (except *autoexec.cfg*, about it below) to your configuration folder along the path `<csgo folder>/csgo/cfg`

In the **autoexec.cfg** file along the path `<csgo folder>/csgo/cfg`, you need to add lines from a similar configuration file in the [Crosshair Manager package] (https://github.com/YakkaDev/CS-GO-Crosshair-Manager/releases/download/v1.1/Crosshair-M.v1.1.rar).

> This file is an autoloader of the parameters of the main game settings file. For experienced players, autoexec is often already in the CS:GO launch options, but if you are a different case, then you need to proceed to the Steam library, then *select CS:GO with RMB - Properties - General - Launch options * and specify `+exec autoexec.cfg`

<p align="center"><img src="/images/launch.png"> </p>

The `bind "key" "changeCrosshair"` line in autoexec.cfg is responsible for switching the crosshair. Replace *key* with your desired key.

---

## Settings

In the **crosshair_UI.cfg** file, you can find the lines `alias cross_tech_primary "exec ..."` and `alias cross_tech_second "exec ..."` having the corresponding prescription inside the file. These aliases point to the configuration files of your sights - the first and second modes, respectively. Here you need to specify the names of your files with the settings of the sight, which must first be placed in a folder along the path `<csgo folder>/csgo/cfg`. For convenience, I use numbering in the names, for example *"crosshair_1.cfg"* and so on.

There is also a universal line `alias cross_tech_other "exec ..."` - this is a common sight for the third and fourth slots, as well as all grenades, except for smoke. The last grenade type is also specified in this file, namely in the "Engine" column and looks like this: `alias cross_tech_smokes "exec crosshair_smokes.cfg"`.

It is recommended not to customize the rest of the binds in the file, since this can lead to the manager's failure to work, or simply does not make any sense.

---

## Config

There are three files in the archive: *"crosshair_1.cfg", "crosshair_2.cfg" and "crosshair_3.cfg"*. These files are exactly the same and are an example of a correct crosshair configuration file.

The following lines should be inside the crosshair configuration file:

```
cl_crosshair_drawoutline "0"
cl_crosshair_dynamic_maxdist_splitratio "0"
cl_crosshair_dynamic_splitalpha_innermod "0"
cl_crosshair_dynamic_splitalpha_outermod "0"
cl_crosshair_dynamic_splitdist "0"
cl_crosshair_friendly_warning "0"
cl_crosshair_outlinethickness "0"
cl_crosshair_t "0"
cl_crosshairalpha "0"
cl_crosshairdot "0"
cl_crosshairgap "0"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairsize "0"
cl_crosshairstyle "0"
cl_crosshairthickness "0"
cl_crosshairusealpha "0"
```

>Note: You do not need to specify the color of the crosshair in the file!

---

## Colors

To change the color of the crosshair, use the commands below:

|   Command     |     Color     |                       Image                                 |
| ------------- | ------------- | ----------------------------------------------------------- |
| cross_red     | Red           | ![Red](/images/colors/cross_red.png "Red")                  |
| cross_green   | Green         | ![Green](/images/colors/cross_green.png "Green")            |
| cross_blue    | Blue          | ![Blue](/images/colors/cross_blue.png "Blue")               |
| cross_black   | Black         | ![Black](/images/colors/cross_black.png "Black")            |
| cross_white   | White         | ![White](/images/colors/cross_white.png "White")            |
| cross_yellow  | Yellow        | ![Yellow](/images/colors/cross_yellow.png "Yellow")         |
| cross_orange  | Orange        | ![Orange](/images/colors/cross_orange.png "Orange")         |
| cross_breathe | Blue-Light    | ![Blue-Light](/images/colors/cross_breathe.png "Blue-Light")|
| cross_pink    | Pink          | ![Pink](/images/colors/cross_pink.png "Pink")               |
| cross_purple  | Purple        | ![Purple](/images/colors/cross_purple.png "Purple")         |
| cross_brown   | Brown         | ![Brown](/images/colors/cross_brown.png "Brown")            |
| cross_chestnut| Chestnut      | ![Chestnut](/images/colors/cross_chestnut.png "Chestnut")   |
