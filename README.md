```diff
- draft for preview only,  work in progress
```

# California Historic Radio Society
## Software Defined Radio @ Winchell Communications Center 




### SDR Setup

* Hardware

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


* Software

In addition to the OEM software for the above hardware, we also have HDSDR and SDRConsole installed on the SDR Demo PC
* Antenna

Discone Antenna for HoC 

<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/Antenna.jpg"
  alt="CHRS SDR Antenna"
  width="300"
  height="300" 
  style="display: inline-block; margin: 0 auto;vertical-align:middle">


### Getting Started 

  - SDR Hardware
    - RSP DUO
    - ELAD
  - SDR Software
    - SDR Sharp
    - Cubic SDR
    - SDR Console
    - HD SDR 
    - XX
    - XX 
    
- Hardware/Software support matrix @ CHRC HOC

| Hardware      | SDR Software     | Comments      |
| :---          |    :----:        |          ---: |
| RSPDuo        | SDR Uno          | OEM Software  |
| ELAD FDM      | FDM SW2          | OEM Software  |
| RSPDuo        | SDR Console      | Freeware      |
| ELAD          | SDR Console      | Freeware      |
| RSPDuo        | HDSDR            | Freeware      |
| ELAD  FDM     | HDSDR            |  Freeware     |  


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
### Decoding data 

* ADS-B

Automatic Dependent Surveillance-Broadcast (ADS-B)
 is an advanced surveillance technology that combines an aircraft's positioning source, aircraft avionics, and a ground infrastructure to create an accurate surveillance interface between aircraft and ATC.

 ADS-B Out works by broadcasting information about an aircraft's GPS location, altitude, ground speed and other data to ground stations and other aircraft, once per second. Air traffic controllers and properly equipped aircraft can immediately receive this information.

Reference resources


[Wikipedia](https://en.wikipedia.org/wiki/Automatic_Dependent_Surveillance%E2%80%93Broadcast)

[sigidwiki](https://www.sigidwiki.com/wiki/Automatic_Dependent_Surveillance-Broadcast_(ADS-B))

[FAA](https://www.faa.gov/about/office_org/headquarters_offices/avs/offices/afx/afs/afs400/afs410/ads-b)

### Instructions for decoding ADS-B at HOC
This ADS-B Decode is configured for RSPDuo. 


Prerequisites
1. Close all SDR Software (SDR Uno or other frontend UI)
2. Ensure the antenna is connected to the 2nd Tuner of the RSP
<img
  src="https://raw.githubusercontent.com/chrs-hoc/chrs-hoc.github.io/main/pic/ads-b-ant.jpeg"
  alt="ADS-B Antenna connection"
  width="300"
  height="300" 
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 5px;
  width: 150px;
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
