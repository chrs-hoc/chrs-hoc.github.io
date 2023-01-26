```diff
- draft for preview only,  work in progress
```

# California Historic Radio Society #
## Software Defined Radio @ Winchell Communications Center ##

Setup/operating instructions for the SDR demo @ CHRS HoC
<details>
  <summary>SDR Hardware</summary>

  ## Hardware ##

  RSP DUO and ELAD FDM are the two SDR hardware models available at CHRS HoC. 

  RSP Duo

  <img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/SDRplay-RSPduo.jpg"
    alt="RSPDUO SDR"
    width="300"
    height="300" 
    style="display: inline-block; margin: 0 auto; vertical-align:middle">

  ELAD

  <img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/elad-fdm-s2.jpg"
    alt="ELAD SDR"
    width="300"
    height="300" 
    style="display: inline-block; margin: 0 auto; vertical-align:middle">

</details>

<details>
<summary>SDR Software</summary> 

  In addition to the OEM software - SDR Uno and FDM SW2 - for the above hardware, we also have [HDSDR](https://www.hdsdr.de/) and [SDRConsole](https://www.sdr-radio.com/console) installed on the SDR Demo PC
</details>

<details>
<summary> Antenna </summary>

Discone Antenna for HoC 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/Antenna.jpg"
  alt="CHRS SDR Antenna"
  width="300"
  height="300" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">

</details>

<details>



<summary> Getting Started </summary>
HoC setup is configured to oprate in the below hardware/software combinations.


| Hardware      | SDR Software     | Comments      |
| :---          |    :----:        |          ---: |
| RSPDuo        | SDR Uno          | OEM Software  |
| ELAD FDM      | FDM SW2          | OEM Software  |
| RSPDuo        | SDR Console      | Freeware      |
| ELAD          | SDR Console      | Freeware      |
| RSPDuo        | HDSDR            | Freeware      |
| ELAD  FDM     | HDSDR            | Freeware     |  


Unlike the respective OEM software, both HD SDR and SDR Console is configured to work with ELAD **and** RSPDuo.

## Starting the SDR ##

Checklist 
* Ensure both SDRs are powered up via the USB to the host PC
* Verify proper antenna connection to the SDR, as it may vary depending on the band/decoder in use


Easiest option is to type in the SDR software name on the search box next to the Windows start button and select the software of your choice.

## SDR Uno/FDM SW2 - Selecting SDR Hardware ##
For SDR Uno and ELAD FDM, they default to their respective OEM hardware.

## HD SDR - Selecting SDR Hardware ##
For HDSDR, the software will prompt you during start-up  to choose the respective EXT_IO DLL to select SDR Hardware

Select:

extio_elad_fdm_6144k_v3_04.dll -  for ELAD

ExtIO_SDRlay_RSPduo.dll - for RSPDuo

[<img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/HDSDR-Select.PNG"
    alt="HD SDR Selection"
    width="70%"
    height="70%">](https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/HDSDR-Select.PNG)

## SDR Console - Selecting SDR Hardware ##

SDR Console provides the SDR selection during start-up on the GUI

[<img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/SDRConsole-select.PNG"
    alt="SDR Console Selection"
    width="70%"
    height="70%">](https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/SDRConsole-select.PNG)



Detailed operating instructions for the SDR Software



</details>

### SDR Play specific plug-ins 
* FRAN 


### Receving audio signals

* AM Broadcast

  - Using RSP DUO
  - Using ELAD

* FM Broadcast


* Weather broadcast 

* SSB 


* WWV


* ATC 
## Decoding data 

### ADS-B

Automatic Dependent Surveillance-Broadcast (ADS-B)
 is an advanced surveillance technology that combines an aircraft's positioning source, aircraft avionics, and a ground infrastructure to create an accurate surveillance interface between aircraft and ATC.

 ADS-B Out works by broadcasting information about an aircraft's GPS location, altitude, ground speed and other data to ground stations and other aircraft, once per second. Air traffic controllers and properly equipped aircraft can immediately receive this information.

Reference resources


[Wikipedia](https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance%E2%80%93Broadcast)

[sigidwiki](https://www.sigidwiki.com/wiki/Automatic_Dependent_Surveillance-Broadcast_(ADS-B))

[FAA](https://www.faa.gov/about/office_org/headquarters_offices/avs/offices/afx/afs/afs400/afs410/ads-b)



Instructions for decoding ADS-B at HOC
ADS-B Decode is configured for RSPDuo. 

Prerequisites
1. Close all SDR Software (SDR Uno or other frontend UI)
2. Ensure the antenna is connected to the 2nd Tuner of the RSP

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ads-b-ant.jpeg"
  alt="ADS-B Antenna connection"
  width="300"
  height="300" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">


### Steps to receive ADS-B

1. Click on the ADS-B folder on the desktop

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ADS-B.PNG"
  alt="ADS-B Antenna connection"
  width="800"
  height="400" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">

2. Doubleclick and start 8I shortcut

You should see a command prompt with the decoded ADS-B Data

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ADSB-1.PNG"
  alt="ADS-B decode"
  width="800"
  height="400" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">

 3. Goback to the ADS-B folder on the desktop and click on Virtual Radar
 It will bring up the virtual Radar UI
 <img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ADSB-2.PNG"
  alt="Virtual Radar"
  width="800"
  height="400" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">

  4. Click on the blue hyperlink on the Virtual Radar UI (http://127.0.0.1:8001/VirtualRadar)

It will bring up the webpage with the ADS-B Data plotted the map

 <img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ADSB-3.PNG"
  alt="Virtual Radar"
  width="800"
  height="400" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">

### Decoding data - audio encoded
#### Basics 
Explanation of basic decoding with virtual audio patch


* CW

* FT8

* WSPR

* ACARS

* ADS-B

* APRS 

* AIS 

* Weather Fax

* ISM/ Utility meter Standard Consumption Message (SCM) 

* Trunked Radio/Digital Audio

* ATCS (TBD) 
