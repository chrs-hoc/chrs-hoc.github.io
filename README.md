```diff
- draft for preview only,  work in progress
```

# California Historic Radio Society #
## Software Defined Radio @ Winchell Communications Center ##

Setup/operating instructions for the Software Defined Radio @ CHRS HoC

Click on the heading to expand each topic

<details>

  <summary>SDR Hardware</summary>

  ## Hardware 

  RSP DUO and ELAD FDM are the two SDR hardware models available at CHRS HoC. 
  
  RSP Duo 

  <img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/SDRplay-RSPduo.jpg"
    alt="RSPDUO SDR"
    width="300"
    height="300">
 

  ELAD

  <img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/elad-fdm-s2.jpg"
    alt="ELAD SDR"
    width="300"
    height="300">

</details>

<details>

<summary>SDR Software</summary> 

On the SDR Demo PC, in addition to the OEM software for the aforementioned devices, we also have [HDSDR](https://www.hdsdr.de/) and [SDRConsole](https://www.sdr-radio.com/console) installed.

</details>

<details>
<summary> Antenna </summary>

Discone Antenna for HoC 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/Antenna.jpg"
  alt="CHRS SDR Antenna"
  width="300"
  height="300">

</details>

<details>



<summary> Getting Started </summary>

The hardware and software combinations listed below are tested at the HoC setup.

| Hardware      | SDR Software     | Comments      |
| :---          |    :----:        |          ---: |
| RSPDuo        | SDR Uno          | OEM Software  |
| ELAD FDM      | FDM SW2          | OEM Software  |
| RSPDuo        | SDR Console      | Freeware      |
| ELAD          | SDR Console      | Freeware      |
| RSPDuo        | HDSDR            | Freeware      |
| ELAD  FDM     | HDSDR            | Freeware     |  


Unlike the respective OEM software, both HD SDR and SDR Console is configured to work with ELAD **and** RSPDuo.

## Starting the SDR 

Checklist 
* Ensure both SDRs are powered up via the USB to the host PC
* Verify proper antenna connection to the SDR

To start the SDR software, type in the SDR software name in the search box next to the Windows start button, then select and start.
## SDR Uno/FDM SW2 - Selecting SDR Hardware 
For SDR Uno and ELAD FDM, they default to their respective OEM hardware.

## HD SDR - Selecting SDR Hardware 
For HDSDR, the software will prompt you during start-up  to choose the respective EXT_IO DLL to select SDR Hardware

Select:

extio_elad_fdm_6144k_v3_04.dll -  for ELAD

ExtIO_SDRlay_RSPduo.dll - for RSPDuo

<img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/HDSDR-Select.PNG"
    alt="HD SDR Selection"
    width="70%"
    height="70%">

## SDR Console - Selecting SDR Hardware 

SDR Console provides the SDR selection during start-up.

<img
    src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/SDRConsole-select.PNG"
    alt="SDR Console Selection"
    width="70%"
    height="70%">



</details>
<details>

<summary>Receiving AM/FM/SSB/NFM</summary>

Decoding AM/FM/SSB/NFM is not covered here, please reference to respective product documentation for the same.

Detailed operating manuals

[SDR Uno](https://www.sdrplay.com/docs/SDRplay_SDRuno_User_Manual.pdf)

[FDM-SW2](https://amd.co.at/anti/afu/FDM_DUO/Manuals/Sw2_user_manual_rev1.01draft.pdf)

[HDSDR](https://www.hdsdr.de/faq.html)

[SDR Console](https://www.sp2put.pl/wp-content/uploads/2017/07/SDR-Console-V2.pdf)

</details>
<details>

<summary> ADS-B </summary>

### ADS-B 

Automatic Dependent Surveillance-Broadcast (ADS-B)
 is an advanced surveillance technology that combines an aircraft's positioning source, aircraft avionics, and a ground infrastructure to create an accurate surveillance interface between aircraft and ATC.

 ADS-B Out works by broadcasting information about an aircraft's GPS location, altitude, ground speed and other data to ground stations and other aircraft, once per second. Air traffic controllers and properly equipped aircraft can immediately receive this information.

Reference resources


[Wikipedia](https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance%E2%80%93Broadcast)

[Sigidwiki](https://www.sigidwiki.com/wiki/Automatic_Dependent_Surveillance-Broadcast_(ADS-B))

[FAA](https://www.faa.gov/about/office_org/headquarters_offices/avs/offices/afx/afs/afs400/afs410/ads-b)


## Instructions for decoding ADS-B at HOC

ADS-B Decode is configured for RSPDuo. 

Prerequisites
1. Close all SDR Software (SDR Uno or other frontend UI).

## Procedure 

1. Open the ADS-B folder on the desktop

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ads-b/ADS-B.PNG"
  alt="ADS-B Antenna connection"
  width="70%"
  height="70%">

2. Doubleclick and run the "start8I" shortcut

In a couple of seconds this will bring up a command prompt with the decoded ADS-B Data.
Since we are close to SFO, it should list several Aircrafts within seconds of starting up.

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ads-b/ADSB-1.PNG"
  alt="ADS-B decode"
  width="70%"
  height="70%">

3. Return to the ADS-B folder on the desktop and start  Virtual Radar.exe which will bring up the Virtual Radar UI

 <img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ads-b/ADSB-2.PNG"
  alt="Virtual Radar"
  width="70%"
  height="70%">

4. Click on the blue hyperlink on the Virtual Radar UI (http://127.0.0.1:8081/VirtualRadar)

That will bring up the webpage with the ADS-B data plotted the map

 <img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ads-b/ADSB-3.PNG"
  alt="Virtual Radar"
  width="70%"
  height="70%">

5. Click on any aircraft to find the details about it.

Note : Close the ADS-B Decoder and command prompt before running other SDR applications. 
Press Control+C on the command prompt to close it. After Control+C Type "Yes" to "Terminate the batch job" prompt on the command window

</details>

<details>
<summary> Trunked Radio Systems</summary>

A trunked radio system is a two-way radio system that uses a control channel to automatically assign frequency channels to groups of user radios.

[Wikipedia - Trunked Radio](https://en.wikipedia.org/wiki/Trunked_radio_system)

[Sigidwiki](https://www.sigidwiki.com/wiki/Category:Trunked_Radio)

[WIkipedia - PL-25](https://en.wikipedia.org/wiki/Trunked_radio_system)

[Radio Reference wiki](https://wiki.radioreference.com/index.php/Trunked_Radio_Systems)

[Alameda country Trunked Radio systems](https://www.radioreference.com/db/browse/ctid/183/trs)



## Instructions for receiving trunked radio at HOC 

Prerequisites
1. Close all SDR Software (SDR Uno or other frontend UI).

## Procedure 

1. Open SDR-Trunk folder on the desktop

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/trunked-radio/sdr-trunk-folder.png"
  alt="SDR Trunk "
  width="70%"
  height="70%">

2. Right click and open the SDR trunk Shortcut 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/trunked-radio/sdr-trunk-open.png"
  alt="SDR Trunk "
  width="70%"
  height="70%">

3. On "Auto start channels" window, click "Start now"

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/trunked-radio/sdr-trunk-start.png"
  alt="SDR Trunk "
  width="70%"
  height="70%">

4. Give it a couple of seconds to initialize and connect to the trunk control channel

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/trunked-radio/sdr-trunk-running.png"
  alt="SDR Trunk "
  width="70%"
  height="70%">
  
  Note : Close SDR Trunk  before running other SDR applications. 
</details>




<details>
<summary> Audio Routing</summary>

Several data transmissions are encoded as audio tones which can be decoded using special software.
In order to accomplish this, we must link the SDR software's audio output to the corresponding decoder software's input. A physical loopback audio cable and two sound cards can be used for this, or you can use specialized software to establish a software audio loopback cable. This will accept the SDR software's audio output and feed it as audio input to any application. In our case, the virtual audio loopback cable or software is being used. To route the SDR software's audio output to the virtual patch connection, follow the steps listed below. 
Decoders will be covered in their respective sections.


[Audio Loopback](https://www.dxzone.com/5-free-virtual-audio-cable-software/)

## Instructions for Audio Routing 
You can use any SDR Software/Hardware to receive the signal (tune) and route the audio to the decoder software
The following lists the procedure for all the SDR software installed on the HOC environment

Prerequisites/notes
1. Default audio out is to the speakers. Routing audio to the virtual cable will disable the speaker output
2. To restore the audio to speakers, follow the same procedure and select "Speakers/Headphones - Realteak" as the output device

## Routing audio from SDR Uno 

1. From SDR Uno Rx control window, click settings
2. In the RX Settings 0-0  window, select "OUT" tab
3. Select "CABLE Input (VB-Audio)" from the dropdown 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/audio-route/sdr-Uno.png"
  alt="Audio Routing"
  width="70%"
  height="70%">

## Routing audio from ELAD

1. Click on the settings button next to the power button icon
2. Select "Audio" tab
3. Select "CABLE Input (VB-Audio)" from the dropdown 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/audio-route/elad.png"
  alt="Audio Routing"
  width="70%"
  height="70%">

## Routing audio from HD-SDR

1. Click on the Sound card \[F5] button 
2. Select "CABLE Input (VB-Audio)" from the Sound card selection window 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/audio-route/hd-sdr.png"
  alt="Audio Routing"
  width="70%"
  height="70%">


## Routing audio from SDR Console

1. Click on the Speaker/Headphones 
2. Select "CABLE Input (VB-Audio)" from the dropdown list

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/audio-route/sdr-console.png"
  alt="Audio Routing"
  width="70%"
  height="70%">

</details>

<details>

<summary> Weatherfax</summary>

Radiofax, also known as HF FAX, radiofacsimile or weatherfax, is a means of broadcasting graphic weather maps and other graphic images via HF radio

[Wikipedia](https://en.wikipedia.org/wiki/Radiofax#Weatherfax)

[NOAA Weatherfax schedule](https://www.weather.gov/media/marine/rfax.pdf)

[Sigidwiki](https://www.sigidwiki.com/wiki/WEFAX)


### Frequency (nearest)

U.S. Coast Guard Communications Station NMC - Point Reyes, CA 

Assigned frequencies 4346, 8682, 12786, 17151.2, 22527 kHz / USB

Select a carrier frequency 1.9 kHz below those listed when using a
single sideband radio in the USB mode to receive these broadcasts.

## Procedure 

1. Tune to the weatherfax station on the SDR, USB (remember to select a carrier frequency 1.9 kHz below the listed)
2. Route the audio to virtual loopbck cable - [Instructions here](#instructions-for-audio-routing)
3. Open multipsk by typing 'Multipsk' on the windows search bar
4. Click on the RX/TX button 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/WeatherFax/start1.png"
  alt="MultiPSK"
  width="70%"
  height="70%">

5. Click on the FAX button to start decoding weather fax

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/WeatherFax/weather-fax.png"
  alt="Weatherfax"
  width="auto"
  height="auto">

</details>

<details>

<summary> APRS - Automatic Packet Reporting System </summary>

Amateur Packet Reporting System (APRS) is a digital communication system utilized by amateur radio operators to exchange messages and track locations utilizing GPS.

[APRS Website](http://www.aprs.org/)

[Wikipedia](https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System)

[Sigidwiki](https://www.sigidwiki.com/wiki/Automatic_Packet_Reporting_System_(APRS))


### Frequency
144.390MHz, NFM

## Procedure 

1. Tune to 144.390MHz, NFM on the SDR
2. Route the audio to virtual loopbck cable - [Instructions here](#instructions-for-audio-routing)
3. Open multipsk by typing 'Multipsk' on the windows search bar
4. Click on the RX/TX button 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/WeatherFax/start1.png"
  alt="MultiPSK"
  width="70%"
  height="70%">

5. Click on the PACKET+APRS Button to start the decode. 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/APRS/MPSK-start-APRS-Text.png"
  alt="MultiPSK"
  width="70%"
  height="70%">

6. Click on the APRS button to show the Map

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/APRS/MPSK-start-APRS-Map.png"
  alt="MultiPSK"
  width="70%"
  height="70%">

</details>
<details>

<summary>Pending</summary>

* CW

* FT8

* WSPR

* ACARS


* AIS 

* ISM/ Utility meter Standard Consumption Message (SCM) 

</details>


