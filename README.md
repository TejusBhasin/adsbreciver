# The ADS-B Receiver Project :airplane:

<img width="3697" height="2221" alt="image" src="https://github.com/user-attachments/assets/be500a60-8119-449a-a88b-0ecc45f436b7" />

BILL OF MATERIALS:
 1 Raspberry Pi 2B or newer (I use the 4b): https://www.pishop.us/product/raspberry-pi-4-model-b-2gb/?srsltid=AU7gw4V_-BQwl1-QtGvcHS5KHYHh5SG0pu57tyJnc7SQvcla4YO7R-n5d_k
 1 Standard Antenna indoors or outdoors, compatible with your ADSB stick: https://www.amazon.com/dp/B009U7WZCA?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1
 1 ADSB Stick configured to 1090ES. Mine came with the antenna: https://www.amazon.com/dp/B009U7WZCA?ref_=ppx_hzsearch_conn_dt_b_fed_asin_title_1
 1 micro SD card, 32gb or more: https://www.amazon.com/SanDisk-Ultra%C2%AE-microSDHC-120MB-Class/dp/B08L5HMJVW/ref=sr_1_4_mod_primary_new?crid=309ETHMK7ASE1&dib=eyJ2IjoiMSJ9.9yRU78cnFSjLUK_rxwTOycx__oNXDnOpDRIkinobDl4WKeXrpxz_QVAkirfNh0jtE6WHFdp6AKlTojfHOX_91Sw3buEVGcaR1-P_wa50Lb7RXne7e_fgUW9Rvt3mi4HKoM6P9xMq1b2Bj9ID88YypJpeqdt7RQS2Tok4i2ARXnIlPsGCu32qCqKVTHaXnq2frNkvhxOs8g8vUdgWy02Ef_kvtL-EDj4Dx1iUsUyHRzbpY_PfsdvSonvsCCm8TrAszU4DKunzkFtGvj24cYrEgnDjhVt-ZiC5Y23VekKcjgs.YbaX0x8hjxgHIYiMVtZwpZ-tYoCJlX74Di24K03OhOQ&dib_tag=se&keywords=32gb+microsd&qid=1789924577&s=electronics&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=32gb+microsd%2Celectronics%2C144&sr=1-4#customerReviews
 
## Easily install ADS-B/UAT/ACARS/VDLM2 related applications!

This project continues to realize that for some, Docker and premade images are not the most optimal solution.

It would seem as of late the move towards premade as well as Docker and other PaaS images with preinstalled software has become popular within the community. Docker images require additional software and, in some cases, result in additional overhead as well as making trivial configuration changes more complicated than they should be. Most of these solutions also come with preinstalled software one may never use as part of the image as well. This project offers the ability to choose and install only what you want or need natively across a wide range of devices with minimal command line experience.

## Obtaining And Using This Software

### New installations...

    sudo apt-get update
    sudo apt-get install git
    git clone https://github.com/jprochazka/adsb-receiver
    cd ~/adsb-receiver
    chmod +x install.sh
    ./install.sh

### Updating existing installations...

Your local repositories master branch will be updated each time install.sh is executed that is unless either the `--development` or `--branch <branch>` switch is used. Unless you are testing an upcoming release or wishing to contribute to the project you will generally not need to use either of these switches.

    cd ~/adsb-receiver
    ./install.sh

## What Can Be Installed

The following software can be installed using these scripts.

### The ADS-B Portal

Included is the option to install the ADS-B Portal which offers the following features.

* Saves all flights seen as well as displays a plot for the flight.
* Saves all ACARS and VDLM2 messages received and offers the ability to view them.
* Control what is displayed online via a web based administration area.
* A more uniform website site layout that can be easily navigated.
* Web accessible dump1090 and system performance graphs.
* Easy access to live dump1090 and dump978 maps.
* A blog which can be used to share your aircraft tracking experiences with others.
* Visitors can be informed when specific flights are being tracked.
* Administrators can be informed via email when specific flights are being tracked.
* Easily customize the look of your portal using the custom template system.

When setting up the portal you will have to choose between a lite or advanced installation. Advanced features add flight logging and plotting and should only be chosen on devices running a sturdy data storage solution.

*It is highly recommended that anyone using a SD card as thier storage medium not attempt to use the advanced features.*

### Decoders

* ACARSDEC:                https://github.com/TLeconte/acarsdec
* Dump1090 (FlightAware):  https://github.com/flightaware/dump1090
* Dump978 (FlightAware):   https://github.com/flightaware/dump978
* Dumpvdl2:                https://github.com/szpajder/dumpvdl2
* Readsb:                  https://github.com/wiedehopf/readsb
* VDLM2DEC:                https://github.com/TLeconte/vdlm2dec

### Feeders

* ADS-B Exchange Feeder Client:   https://adsbexchange.com
* AirNav Radar Client:            https://airnavradar.com
* Airplanes.live Feeder Client:   https://airplanes.live
* FlightAware's PiAware:          https://flightaware.com
* Flightradar24 Feeder Client:    https://flightradar24.com
* Fly Italy ADS-B Feeder Client:  https://flyitalyadsb.com
* OpenSky Feeder Client:          https://opensky-network.org
* Plane Finder ADS-B Client:      https://planefinder.net

### Extras

* Beast-Splitter:       https://github.com/flightaware/beast-splitter
* DuckDNS.org Support:  https://www.duckdns.org
* Graphs1090:           https://github.com/wiedehopf/graphs1090
* tar1090:              https://github.com/wiedehopf/tar1090

## Supported Operating Systems

The project currently supports the following Linux distributions.

* Raspberry PI OS _(Legacy, Current)_
* Debian _(Bookworm, Trixie)_
* Ubuntu _(Jammy Jellyfish, Noble Numbat, Questing Quokka)_

_These scripts should work most any Debian based distributions_

Support is available via this repository through the use of the issue tracker or discussions.
