# HOME

> [!WARNING|style:flat|label:Result of unofficial sources|iconVisibility:visible]
>
> Gaggiuino Gen 3 is free to use and will offer free software updates, but the source code is no longer available.  
> This decision was made to maintain high standards for the hardware required for the project and prevent individuals from fracturing the community with subpar, non-standard components and processes that were untenable for Gaggiuino’s community-driven support to accommodate.
>
>Sincerely,
>
>The GAGGIUINO Team

> [!Info]
> When buying from any of the approved suppliers you can head over to the community [Discord](community/community-media.md#community-discord) for order updates or install-help in the relevant channels.
> 
> Relevant channels for orders : #diy-efi-co-uk, #peakcoffee-cc, #espressio-nl
> 
> Relevant channels for install-help: #install-help-xxx



**Contribute to the project development efforts.**
<!-- ko-fi :id=zer0bit :color=<color> -->
    Support the development efforts
<!-- ko-fi -->
>
# Features

Advanced pressure and flow profiling, web interface, shot history, OTA updates, Bluetooth scales... so many features we decided to put them under a dropdown. If you want to dive in, expand below!

<details>
<summary><b>Gaggiuino Features Comparison</b> <i>(Click to expand)</i></summary>

  Feature                |Gen 1<br/>Nano & Nextion|Gen 2<br/>STM32 & Nextion|Gen 3<br/>STM32 & ESP32
-----------------------  |:----------------------:|:-----------------------:|:----------------------:
  Neat integration       |:heavy_check_mark:|:heavy_check_mark:  |:heavy_check_mark:      
  Embedded UI            |:heavy_check_mark:|:heavy_check_mark:  |:heavy_check_mark:       
  Full temp control      |:white_check_mark:|:white_check_mark:  |:heavy_check_mark:       
  Auto Shot Timer        |:heavy_check_mark:|:heavy_check_mark:  |:heavy_check_mark:       
  Graphing               |:white_check_mark:|:white_check_mark:  |:heavy_check_mark:                
  Pressure profiling     |:white_check_mark:|:white_check_mark:  |:heavy_check_mark:   
  Manual flow control    |:white_check_mark:|:heavy_check_mark:  |:heavy_plus_sign:       
  Settings persistence   |:white_check_mark:|:heavy_check_mark:  |:heavy_check_mark: 
  Descale program        |:white_check_mark:|:white_check_mark:  |:heavy_check_mark:  
  Integrated scales      |:white_check_mark:|:heavy_check_mark:  |:heavy_check_mark: 
  Stop on Weight/Dose<sup> 1</sup>|:x:      |:heavy_check_mark:  |:heavy_check_mark:       
  DreamSteam<sup> 2</sup>         |:x:      |:white_check_mark:  |:heavy_check_mark:  
  Predictive scales<sup> 3</sup>  |:x:      |:white_check_mark:  |:heavy_check_mark:            
  Flow profiling         |:x:               |:heavy_check_mark:  |:heavy_check_mark:  
  Advanced profiling     |:x:               |:white_check_mark:  |:heavy_check_mark:  
  Profile Management     |:x:               |:white_check_mark:  |:heavy_check_mark:    
  Unlimited<sup> 4</sup> profiling  |:x:    |:x:                 |:heavy_check_mark:
  Unlimited<sup> 4</sup> phases     |:x:    |:x:                 |:heavy_check_mark:
  Advanced phase limits  |:x:               |:x:                 |:heavy_check_mark:
  Bluetooth scales<sup> 5</sup>    |:x:     |:x:                 |:heavy_check_mark:
  Profiles sharing       |:x:               |:x:                 |:heavy_check_mark: 
  Web interface          |:x:               |:x:                 |:heavy_check_mark: 
  OTA updates            |:x:               |:x:                 |:heavy_check_mark: 
  REST API               |:x:               |:x:                 |:heavy_plus_sign: 

__Explanation__       
:white_check_mark: Available in a limted form             
:heavy_check_mark:  Available      
:x:  Not available       
:heavy_plus_sign: Planned   
>
_1_ __Stop on Weight/Dose__ - stops at a desired yield.  
_2_ __DreamSteam__ - software driven steam boosting.  
_3_ __Predictive scales__ - software driven predicted weight output.  
_4_ __Unlimited__ - probably has a limit, but we haven't found it yet.   
_5_ __Bluetooth scales__ - [find the currently supported scales here](https://github.com/kstam/esp-arduino-ble-scales?tab=readme-ov-file#bluetooth-scales-library-for-esp-on-arduino-framework).   

</details>

>

# Compatibility

Gaggiuino is designed for the Gaggia Classic family of espresso machines with 3-way valves (**NOT the Gaggia Classic V2, SIN035U RI9403**). Other espresso machines such as the Rancilio Silvia are also supported although no official installation instructions are available at this time.  
Gaggiuino is **not** designed for espresso machines that use a heat exchanger, thermoblock, thermocoil, group/check valve,  or rotary pump.  

Name                                      | Voltage   | Model Years | Model ID        | Notes  
------------------------------------------|-----------|-------------|-----------------|-------
:heavy_check_mark: Gaggia Classic         | 100-120 V | 1991-2018   | SIN035 RI9303   | Needs [Grounding](guides/machine-specific-guide.md#grounding) 
:heavy_check_mark: Gaggia Classic         | 220-240 V | 1991-2014   | SIN035 RI9303   |  
:x:                Gaggia Classic V2      | 220-240 V | 2015-2018   | SIN035U RI9403  | <details><summary><b>Avoid like the plague</b> <i>(Click for image)</i></summary><img width="600" alt="image" src="https://github.com/GAGGIUINO/gaggiuino.github.io/assets/117388662/4170cdbf-aebc-4e09-bafa-3f9b5e95a5bb"></details> 
:heavy_check_mark: Gaggia Classic Pro     | 100-120 V | 2019-2022   | SIN035R RI9380  | 
:heavy_check_mark: Gaggia Classic Pro     | 220-240 V | 2019-2022   | SIN035R RI9380  | Uncommon, easier to mod than models with eco PCB
:heavy_check_mark: Gaggia Classic Pro Eco | 220-240 V | 2019-2022   | SIN035UR RI9480 | [Power switch mod](guides/machine-specific-guide.md#power-switch-mod) required and custom wiring recommended due to eco PCB
:heavy_check_mark: Gaggia Classic Evo Pro | 100-120 V | 2023-?      | SIN035R RI9380  | 9 bar OPV must be changed to be a [10-12 bar OPV](guides/machine-specific-guide.md#10-12-bar-opv) <br /> High-temp insulation required for [combined connector insulation](guides/machine-specific-guide.md#combined-connector-insulation) when doing stock wiring integration 
:heavy_check_mark: Gaggia Classic Evo Pro | 220-240 V | 2023-?      | SIN035UR RI9481 | [Power switch mod](guides/machine-specific-guide.md#power-switch-mod) required and custom wiring recommended due to eco PCB

> [!Note|style:callout|label:New Gaggia Classic Pro|iconVisibility:visible]
> The Gaggia Classic Pro E24 has been released to some regions. It's reported that this model is a Gaggia Classic Evo Pro with a new brass boiler, so all notes regarding the Evo *should* apply.  
> The table will be updated when more info is available and we've been able to confirm there are no unexpected deviations.    

>

# Build Process

> [!TIP|style:callout|label:WHERE TO GO FOR HELP|iconVisibility:visible]
> If you need help (even during the planning phase) please make **one** [Discord](community/community-media.md#community-discord) help thread in [#install-help-gc](https://discord.com/channels/890339612441063494/996814638471708683) (for Gaggia Classic) or [#install-help-gcp](https://discord.com/channels/890339612441063494/996188987964268555) (for Gaggia Classic Pro/Eco/Evo).  
> Title the thread by *[username][machine type][control system] Thread Title* and include any links/pictures/videos that may apply to your question. As you have more questions, rename the *Thread Title* and add your question to the thread.  
> ***One help thread per person/machine, please!***

1. **Identify your espresso machine (or determine what to buy)**

  See the [Compatibility Table](#compatibility) and take note of any [Machine-Specific Instructions](guides/machine-specific-guide.md) that are mentioned there. 

2. **Determine your build path.** 

  Decide if you're going to order a [PCB](guides-stm32/pcb-guide.md) or build a [component (Lego)](guides-stm32/lego-component-build-guide.md) control system. PCBv4 is recommended for new Gen 3 builds, while PCBv3.1 is recommended for Gen 2 builds (see [Features](#features) and [Announcements](announcements/) to compare Gen 2 and Gen 3). The component build is slightly more flexible for experimentation and less picky about thermocouple grounding, however, it adds significant effort and makes reliability dependent on the maker's skill. 

  Decide how to integrate the control system with your espresso machine. It can either be [integrated into the stock wiring](guides-stm32/3pln-stock-wiring-integration.md) with a few jumpers (less wiring, but sometimes more confusing) or the stock wiring can be replaced with a [custom wiring harness](guides-stm32/3pln-custom-wiring.md) (more work, but results in a clean, straightforward install). It is recommended that you check the notes in the [Compatibility Table](#compatibility) for your machine and and read through the instructions before deciding.

  If you're building Gen 3, decide which interface option you prefer. Currently there is a 4.3" IPS [touchscreen](guides/interface-screen.md) (embedded and web UI) with 3 mounting options. A headless option (web UI only) is in development.

3. **Select and Order Components**

  Order components based on your machine and install path. Make sure to check the [Bill of Materials](#bill-of-materials), the [custom wiring page](guides-stm32/3pln-custom-wiring.md) (if that's the route you're going), and the pages of any optional accessories ([HW Scales](accessories/hw-scales.md), [ToFnLED](accessories/tofnled.md)) that you'd like to install. 

  There are approved official suppliers for PCBs and Kits, and 3D printed parts linked in the sidebar. Select the 3D print provider closest to you for the lowest shipping cost. Alternatively, the BOM has sources linked so you can order components yourself and 3D print from the design files.

  > [!TIP|style:callout|label:NAMING TIP|iconVisibility:visible]
  > There are two main groups of Gaggia Classic espresso machines referred to in the BOM and instructions:  
  >   - Gaggia Classic (GC)  
  >   - Gaggia Classic Pro (GCP), which generally includes the Pro, Eco, and Evo models

4. **Parts are in, time to build!**

  > [!WARNING|style:callout|label:WARNING ABOUT VIDEOS|iconVisibility:visible]
  > There are no official build videos. It is highly recommended to only follow the instructions on this website.

  Follow the instructions for your control system selection

    * [A: PCB](guides-stm32/pcb-guide.md)
    * [B: Component (Lego) build](guides-stm32/lego-component-build-guide.md)

  Follow the instructions for your wiring selection

    * [A: Stock Wiring Integration](guides-stm32/3pln-stock-wiring-integration.md)
    * [B: Custom Wiring Harness](guides-stm32/3pln-custom-wiring.md)

  Follow the instructions for your interface selection

    * [Interface: Screen](guides/interface-screen.md)

  Follow the instructions for any accessories that may have been selected

    * [HW Scales](accessories/hw-scales.md)
    * [ToFnLED](accessories/tofnled.md)

5. **Make Coffee!**

  Record your first start. Post this to [#first-start](https://discord.com/channels/890339612441063494/919183771079692328) on Discord.  
  Record your first shot. Post this to [#first-shot](https://discord.com/channels/890339612441063494/910972035205857320) on Discord.  
  Read the [User Manual](learning/user-manual.md) for more information on the machine capabilities.  
  Check out [Espresso Aficionados](https://espressoaf.com/guides/profiling.html) for info on profiling that you can now implement!  

<!-- panels:start -->
<!-- div:title-panel -->
# Bill of Materials

> [!TIP|style:callout|label:Sourcing|iconVisibility:visible]
> PCBs, kits, and 3D-printed parts may be ordered from the **Official Group Buy Facilitatiors** in the sidebar.  
> Alternatively, components can be ordered from AliExpress and parts can be printed from the design files (except Gen3 Screen). 

Sourcing Method:
<details>
<summary><b>Group Buy Kits</b> <i>(Click to expand)</i></summary>
<!-- tabs:start -->

<!-- tab:Peak Coffee -->
<!-- tabs:start -->
<!-- tab:Complete Kit (Gen3, Stock Wiring) -->
[Disclaimer](BOM_Breakout/BOM_Markup.md#MODELDISCLAIMER ':include')
**Complete Standard (Stock Wiring)**
This kit comes with the Regular Kit (Gen3) plus the following:
* Pre-soldered dualScales board Kit (everything except 3D Prints)
* TofnLED Kit (everything except 3D Prints)
* Expedited shipping included in price

[Some Name](BOM_Breakout/BOM_Markup.md#OtherPurchasesPEAK ':include')

**Complete Premium** This kit comes with the Regular Kit (Gen3) plus the following:
* Pre-Flash with Modules Enabled
* Soldered DualScaleBoard + Resin reinforced 
* Hose Cutter – V shape blade
* Mini Flat Head – Screw driver
* SanDisk Ultra 32GB SD
* Tested before shipment ( PCB / IoT Touch Screen / USB ST-Link Flasher )
* Extra 4.3″ IoT LCD to PCB Cable
* Special custom made – PCB flashing Cable ( 24 AWG – 45cm )
* WAGOs connectors
* Expedited Shipping Included

[whatElse](BOM_Breakout/BOM_Markup.md#OtherPEAKCOMPLETEPREMIUM ':include')

<!-- tab:Regular Kit (Gen3, Stock Wiring) -->
[Disclaimer](BOM_Breakout/BOM_Markup.md#MODELDISCLAIMER ':include')
Comes with most of the parts you need to do a Gaggiuino stock wiring integration
[Some Name](BOM_Breakout/BOM_Markup.md#OtherPurchasesPEAK ':include')
[ToConsider](BOM_Breakout/BOM_Markup.md#ThingsToConsider ':include')

<!-- tab:IoT Upgrade Kit -->
Use this kit only if you've got an existing Gaggiuino install you want to upgrade OR are self sourcing all other components.
<!-- tabs:end -->

<!-- tab:DIY-EFI -->
<!-- tabs:start -->
<!-- tab:V4 PCB Kit (Gen3, Custom Wiring) -->
[Disclaimer](BOM_Breakout/BOM_Markup.md#MODELDISCLAIMER ':include')
[Disclaimer2](BOM_Breakout/BOM_Markup.md#DIYHVDISCLAIMER ':include')
**Custom Wiring Ordering List**

[Disclaimer3](BOM_Breakout/BOM_Markup.md#CustomWiringDiscl ':include')
[CustomWiring](BOM_Breakout/BOM_Markup.md#CustomWiring ':include')

[WhatElse](BOM_Breakout/BOM_Markup.md#DIYOtherPurchases ':include')
[ToConsider](BOM_Breakout/BOM_Markup.md#ThingsToConsider ':include')
<!-- tab:V4 PCB Kit (Gen3, Stock Wiring) -->
[Disclaimer](BOM_Breakout/BOM_Markup.md#MODELDISCLAIMER ':include')
[Disclaimer2](BOM_Breakout/BOM_Markup.md#DIYHVDISCLAIMER ':include')
**Stock Wiring Ordering List**
[StockWiring](BOM_Breakout/BOM_Markup.md#StockWiring ':include')
[WhatElse](BOM_Breakout/BOM_Markup.md#DIYOtherPurchases ':include')
[ToConsider](BOM_Breakout/BOM_Markup.md#ThingsToConsider ':include')
<!-- tabs:end -->

<!-- tabs:end -->

</details>


<details>
<summary><b>Self Sourcing</b> <i>(Click to expand)</i></summary>




<!-- tabs:start -->
<!-- tab:STM32 PCB -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#SelfSourcePCB ':include')


<!-- tab:STM32 LEGO -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#SelfSourceLEGO ':include')
<!-- tabs:end -->

<!-- tabs:start -->
<!-- tab:Gaggia Classic -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#SelfSourceGC ':include')
<!-- tab:Gaggia Classic Pro -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#SelfSourceGCP ':include')
<!-- tabs:end -->

<!-- tabs:start -->
<!-- tab:Stock Wiring Integration -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#StockWiring ':include')

<!-- tab:Custom Wiring -->
[Disclaimer3](BOM_Breakout/BOM_Markup.md#CustomWiringDiscl ':include')
[CustomWiring](BOM_Breakout/BOM_Markup.md#CustomWiring ':include')

<!-- tabs:end -->

<!-- tabs:start -->
<!-- tab:Gen 3 -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#SelfSourceGEN3 ':include')

<!-- tab:Gen 2 -->
[SelfSourcing](BOM_Breakout/BOM_Markup.md#SelfSourceGEN2 ':include')
<!-- tabs:end -->
<!-- div:panel-end -->

</details>

>


# 3D Printed Parts

BOM and assembly instructions for the recommended 3D printed parts used in the standard install are linked here.  

<!-- tabs:start -->
<!-- tab:STM32 PCB -->
* [PCBv3.1/v4 Housing](https://www.printables.com/model/894339) **OR** [PCBv3 Protective Housing](https://www.printables.com/model/370513)
<!-- tab:STM32 LEGO -->
* [Internal Component Housing](https://www.printables.com/model/269394)
<!-- tabs:end -->

<!-- tabs:start -->
<!-- tab:Gen 3 -->
* [Gen 3 Screen Housing](https://www.printables.com/model/356026)  
  There are 3 mount options that all use the same screen housing. Pick one.  
  <img width="500" alt="image" src="https://github.com/user-attachments/assets/888b31f2-d0e5-48d8-af31-7133bd122f70">
  
  <!-- tabs:start -->
  <!-- tab:Front Mount -->
  * 6 [20x10x3 mm magnets](https://www.aliexpress.com/item/3256803170039630.html)
  * [Kapton tape, 20 mm wide](https://www.aliexpress.com/item/3256803012935630.html)
  * Cyanoacrylate (super glue) or Epoxy

  > [!TIP|style:callout|label:Non-magnetic Machines|iconVisibility:visible]
  > For non-magnetic espresso machines, sub double-sided tape with a long-term temp rating of at least 80° C for the magnets
  > * VHB 4611/5952/4910, Gorilla Tape, Alien Tape are options

  <!-- tab:Funnel Mount -->
  * 3 [M3x30 socket head cap screws](https://www.aliexpress.com/item/2251832782719381.html)
  * 5 [M3 washers (OD ≤7 mm)](https://www.aliexpress.com/item/3256804576158708.html)
  * 5 [M3 split lock washers](https://www.aliexpress.com/item/2251832789389968.html)
  * 2 [M3 nylock nuts](https://www.aliexpress.com/item/2251832802681129.html)
  * 1 [M3 Heat Set Insert Nut, 4.5 or 4.6 mm OD, 5 or 6 mm L](https://www.aliexpress.com/item/3256804684678316.html)
  * Cyanoacrylate (super glue) or Epoxy
  <!-- tab:Rear Mount -->
  * 2 [M3x30 socket head cap screws](https://www.aliexpress.com/item/2251832782719381.html)
  * 4 [M3 washers (OD ≤7 mm)](https://www.aliexpress.com/item/3256804576158708.html)
  * 4 [M3 split lock washers](https://www.aliexpress.com/item/2251832789389968.html)
  * 2 [M3 nylock nuts](https://www.aliexpress.com/item/2251832802681129.html)
  <!-- tabs:end -->
<!-- tab:Gen 2 -->
* [Screen Enclosure](https://www.printables.com/model/280617)
  * 2 M4x10 button-head screws
  * 2 M4 nuts
<!-- tabs:end -->

If you'd like to print the files yourself instead of purchasing from the official suppliers **please carefully review the recommended print parameters** on the design pages.

Additional Gaggiuino models can be found in the [Gaggiuino Model Collection](https://www.printables.com/social/340492-loogle/collections/265668) or on [Discord](community/community-media.md#community-discord) in the **#mod-3d-design-ideas** channel.
>

# Accessories

Accessories can be added to the base Gaggiuino build for additional features. BOM and instructions are linked below. 

* [Hardware Scales](accessories/hw-scales.md) sit below the drip tray and measure weight during shots. They're most useful for those who like to experiment with beans, grind, and profiles where predictive scales may have a difficult time
* [ToFnLED](accessories/tofnled.md) provides an RGB LED and sensor for measuring water tank level

# Contributors

Thank you to everyone who has contributed to the project!

<a href="https://github.com/Zer0-bit/gaggiuino/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Zer0-bit/gaggiuino" />
</a>
<a href="https://github.com/GAGGIUINO/gaggiuino.github.io/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=GAGGIUINO/gaggiuino.github.io" />
</a>

Made with [contrib.rocks](https://contrib.rocks).

# Statistics

<details>
<div>
<a href="https://flagcounter.me/details/dj0"><img src="https://flagcounter.me/dj0/" alt="Flag Counter"></a>
</div>
</details>
