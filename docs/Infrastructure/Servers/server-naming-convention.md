# Server Naming Convention

## Intro
Why not have fun with naming some of the servers that we're using? This is a list of potential and used names for our servers, sorted (kinda) by category.  
Names are sorted by what type of server they could be used for (or are planned for). If a name is used, there will be an icon next to it (see key below), and a link to its detail page.

These names are drawn from a variety of sources, including the following:  
- [jparill's hostname_servers list](https://gist.github.com/jparrill/6971533)  
- [namingscemes.com](https://namingschemes.com/Main_Page)  

### Icon Key
A full list of icons used, with details, is available at [:material-arrow-right:Icons Used on this Wiki](../../Meta/mkdocs.md).

:octicons-server-24: - a generic server that we don't have a better icon for yet.  
:octicons-container-24: - a hypervisor server hosting other little servers. [:material-egg-easter:](https://black-cat-labs.b-cdn.net/memes/shipping-ship.jpg)  
:material-wall-fire: - a firewall (either server or dedicated hardware)  
:material-router-network: - a network router (either server or dedicated hardware)  
:material-backup-restore: - a backup server  
:octicons-graph-24: - a monitoring server

## :octicons-server-24: Servers
### If virtualized within our own hardware
Need to come up with a specific convention for this, but it's going to be something like client name (if applicable) + service name or type + OS + number.  
For example: `WidgetCo-Nextcloud-Ubuntu-01`.

!!! warning "Heads up"
    This naming convention is subject to change after I do some research and see if I can find a better practice for naming these.

It's not quite as fun, but makes wrangling things a little easier than names within names.

### If physical or on a hosted VPS
#### U.S. Lakes
??? abstract "U.S. Lakes list"
	- ~~Action~~
	- [Alturas :octicons-container-24:](<Server Inventory/alturas.md>)
	- Baron
	- Bantam
	- Beaver
	- Beshear
	- Bluestone
	- Bluewater
	- Burke
	- Caddo
	- Candlewood
	- Cedar
	- Champlain
	- Claytor
	- Como
	- Cowan
	- Crater
	- Crescent
	- Crystal
	- Cumberland
	- Cypress
	- Degrar
	- Delta
	- Donner
	- Eagle
	- Elk
	- Elwell
	- Emporia
	- Enid
	- Erie
	- Fairfax
	- Fallriver
	- Fenton
	- Geneva
	- George
	- Greenbo
	- Greers
	- Greerson
	- Gull
	- Harding
	- Harris
	- Hartwell
	- Hauser
	- Heron
	- Higgins
	- Holt
	- Horsehead
	- Houghton
	- Huron
	- Isabella
	- Kickapoo
	- Kissimmee
	- Leech
	- Liberty
	- Locust
	- Lurleen
	- Marion
	- Meade
	- Merritt
	- Michigan
	- Minnetonkas
	- Mono
	- Navajo
	- Okeechobee
	- Ontario
	- Ozarks
	- Patoka
	- Peck
	- Perry
	- Placid
	- Pleasant
	- Pontchartrain
	- Powell
	- Pyramid
	- Redfish
	- Rend
	- Rico
	- Rush
	- Sabbatia
	- Sabine
	- Sakakawea
	- Salton
	- Sardis
	- Saugatuck
	- Sawtooth
	- Seeley
	- Seminole
	- Sevuer
	- Shasta
	- Sinclair
	- Spirit
	- Storm
	- Stump
	- Summer
	- Sunapee
	- Superior
	- Sutton
	- Tahoe
	- Texoma
	- Travis
	- Trinity
	- Tule
	- Tupper
	- Tygart
	- Ute
	- Verret
	- Walker
	- Walloon
	- Wheeler
	- Wilson
	- Zoar

## :material-wall-fire: Firewalls
### If virtualized (e.g. OPNsense)
The firewall gets the name of server it's virtualized on, plus `FW` plus the number of the firewall for that server.  
For example, if there's only one firewall on a server named `Sawtooth`, then it would be named `Sawtooth-FW-01`.

It's not quite as fun, but makes wrangling things a little easier than names within names.

### If hardware
#### Prisons
??? abstract "Prisons list"
	- Alcatraz
	- Angola
	- Attica
	- Bautzen
	- Bastille
	- Bangkwang
	- Belmarsh
	- Brushy
	- Bucca
	- Cropper
	- Dartmoor
	- Devil
	- Durham
	- Florence
	- Folsom
	- Ghuraib
	- Guantanamo
	- Lancaster
	- Levenworth
	- Marion
	- Reading Gaol
	- Riker
	- Robben
	- Shawshank
	- SingSing
	- Wandsworth
	- Wormwood
Curated from [https://namingschemes.com/Prisons](https://namingschemes.com/Prisons).

## :material-router-network: Routers
### If virtualized (e.g. OPNsense)
The firewall gets the name of server it's virtualized on, plus `RTR` plus the number of the firewall for that server.  
For example, if there's only one firewall on a server named `Meade`, then it would be named `Meade-RTR-01`.

It's not quite as fun, but makes wrangling things a little easier than names within names.

!!! info "A note on combined firewalls and routers"
    Since we frequently are combining firewall and router (e.g. OPNsense), you may have a server that could use both the `FW` and the `RTR` tag.

    In this instance, use **only** the `FW` tag, and **not** the `RTR` tag. Do not combine them to `FWRTR` or anything like that.

### If hardware
#### 57 Selected Stars for Navigation
??? abstract "57 Selected Stars for Navigation list"
	- Achernar
	- Acamar
	- Acrux
	- Achernar
	- Adhara
	- ~~Al Na'ir~~
	- Aldebaran
	- Alkaid
	- Alnilam
	- ~~Alpha~~ Capricorni
	- Alpheratz
	- Altair
	- Alphecca
	- Alphard
	- Alpheratz
	- Altair
	- Ankaa
	- Antares
	- Arcturus
	- Atria
	- Avior
	- Bellatrix
	- Betelgeuse
	- Canopus
	- Capella
	- ~~Deneb~~
	- Denebola
	- Diphda
	- Dubhe
	- Eltanin
	- Enif
	- Elnath
	- Fomalhaut
	- Gacrux
	- Gienah
	- Hadar
	- Hamal
	- Kaus
	- Kochab
	- Markab
	- ~~Menkar~~
	- Menkent
	- Miaplacidus
	- Mirfac
	- Nunki
	- Peacock
	- Pollux
	- Procyon
	- Rasalhague
	- Regulus
	- Rigel
	- ~~Rigil~~ Kentaurus
	- Sabik
	- Schedar
	- Shaula
	- Sirius
	- Spica
	- Suhail
	- Vega
	- Zubenelgenubi
Curated from [https://namingschemes.com/57_Selected_Stars_for_Navigation](https://namingschemes.com/57_Selected_Stars_for_Navigation).

## :material-backup-restore: Backup Servers
### Poisons
??? abstract "Poisons list"
    - Arsenic
    - Cyanide
    - Hemlock
    - Latex
    - Nightlock
    - Thallium

## :octicons-graph-24: Monitoring Servers
### D&D Monsters
??? abstract "D&D Monsters list"
    - Beholder
    - Bugbear
    - Chimera
    - Digester
    - Elemental
    - Gargoyle
    - Ghoul

Curated from [https://namingschemes.com/Dungeons_and_Dragons_Monsters](https://namingschemes.com/Dungeons_and_Dragons_Monsters).