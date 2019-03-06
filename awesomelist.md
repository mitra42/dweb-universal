# Awesome list - Content Access

This is a list of projects and resources relevant to 
the goal of the Dweb-Universal project of
getting content to places where the internet is of low quality 
either through cost, speed, or censorship. 

## Guides to contributing
It is curated by Mitra, but with additional curation welcome,
and especially please edit your own entry, or send me a replacement
and any other updates, additions & corrections.

The attribution of sources is partly to give credit, but also a hint as to who might have done further research.

Contact info for contributors is at the bottom.
  
Last update: Mitra 2019-02-10

## Categorisation

As engineers we love to categorize and organize things into stacks, so here's my completely arbritrary stack.

* Hardware: Physical devices things run on
* Content: Without content there's nothing to look at, this includes aggregators like the Internet Archive, or Wikipedia
* Servers/Apps: Usually tied to a specific set of content, or to a content standard
* Platforms: Software that ties together Servers, Hardware management, admin, access etc with some kind of UI
* Implementers: Orgs that take the Platforms and install them in some underserved location.
* Internet Access: Getting the local access, and backhaul to the global internet working, includes mesh networking, satellite links, and local nodes etc

### Summary Table

Org or Project|Categories|Builds on|Type|Notes
---|-------|----|----|-----
Altermundi|Implementers|Libremesh|?|Argentina, Mexico remote villages
Blupoint|Platform?|?|?|Audio only
Bluetown|Platform / Implementers|?|For Profit|
Coolabs|Platform|Ambien, TV boxes|Non-profit ?|
EduAir|Platforms|?|?|Cameroon formerly Kwiizi
eGranary|Platforms|Windows|?|Confusingly also called Internet In A Box
eLimu|Content|?|?|
FreedomBox|?|?|?|
Guifi|Internet|Libremesh|?|Catalonia
IEEE Sight|?|?|?|Tunisia
Imcon|?|?|?|
Internet Archive|Content+Server| |Non-profit|
KA Lite|Servers|Khan Academy|project of Learning Equality|
Kolibri|Servers|OER|project of Learning Equality|
Internet in a Box|Platform|RPi; which servers?|Non-profit ?|
Kiwix|Servers|Wikipedia|?|App
Kolibri|Servers|OER|
LearningEquality|Servers|Kolibri, KA Light|Non profit|Developers of Kolibri & KA Light
Libremesh|Internet|?|?|WiFi mesh software
Mikrotik|Platform|?|?|
Onno Purbo|Platform|RPI; which services?|?|Indonesia
Pfsense|Platform|?|?|
PirateBox|Platform|RPi|?|Offline (WiFi) file sharing
Pnkgo|Platform|RPi, Microtik, Ubiquity|?|Focus on disasters
Rachel|Hardware+Platform|OER2GO, Kolibri, Intel device|Non-profit|
Rhizomatic|Implementers + Internet Access ?|? RPi|
Widernet|See eGranary

# Organizations and Projects
##### in Alphabetical order

### Altermundi
Building WiFi mesh networks in remote villages (Argentina ?, Mexico). 
Uses [libremesh](https://chef.libremesh.org/) for mesh, RPi for local servers.
Contact: Nico Pace

### Blupoint 
BluePoint Integrated content delivery through meshwifi/GSM/bluetooth... including offline environments http://bluepoint.org
Audio based; seems like a bit of a closed-system (curated content only) but I might be misreading that,
or there might be specific applications. MikeJ said: It is a UK business, but their strategy, and goals of working on feature phones, fm radio is worth noting - particularly as I had already planned to talk to you about the potential for audio content delivery.... 
[blupoint.org](https://www.blupoint.org/why-blupoint/)
 -- from Mike Jensen 2018-11

### Bluetown
Village networks - VSat backhaul, local wireless, captive portal.
Local content paid by sponsors (typically government); PAYG for access to internet
-- Mitra 2018-11

### Coolabs (TODO need link)
Location: near Sao Paolo?

A group of hardware hackers / community network folks where they have local / offline services, 
and are experimenting with tv box for serving local content which is cheaper than RPi 
They are using the  EGGOIGO 'smart tv' - see https://xsreviews.co.uk/reviews/egoiggo-s95x-smart-tv-box-review/
Contacts: Hiure Quiroz (developer) & Bruno
 
IA next steps: Mitra Scheduling call with Bruno

### EduAir (Formerly Kwiizi) from Cameroon
is the concept name to offer a better education via digital with or without the internet. Their work focuses on the design of portable and open media libraries in the form of Boxes with solar energy giving access to millions of educational content and offering an integrated communication system where learners can make video calls within the local network deployed by the Box http://www.eduair.org -- from Mike Jensen 2018-11

### eGrannary / Widernet - NC USA
Platform - works on window, also called Internet in a Box, but no obvious relationship. Clif Missan
-- Mike Jenson Jan2019

IA next steps: reach out

### eLimu
Educational agency, eLimu, which creates digital educational material in fun formats, including animations, film and puzzles. 
Used in the Kibera Library project (Kenya) 
-- from Mike Jensen 2018-11

### FreedomBox

### Guifi - Catalonia
Largest WiFi mesh network - Catalonia - uses Libremesh. 
Mostly not actually meshing, but extending higher bandwidth fixed connections over WiFi to third parties, i.e. they have the payment/sharing part working.

### IEEE Sight in Tunisia
developed Raspberry Pi operated devices with hard disks that can be updated periodically with relevant content such as Wikipedia pages, TED Talks and other educational content from the Internet. They are capable of automatically updating content when connected to Wi-Fi or 3G networks.
[1worldconnected.org/wp-content/uploads/2018/02/Project-Tawasol-Tunisia.pdf](Project-Tawasol-Tunisia.pdf)
-- from Mike Jensen 2018-11

### Imcon International 
https://imconintl.com/product/edu/ - from Mike Jensen 2019-01-04

### Internet Archive - [archive.org](https://archive.org), [dweb-universal](https://github.com/internetarchive/dweb-universal). 
Almost all our content is in the public domain.  
Currently working on a server to enable offline access [dweb-mirror](https://github.com/internetarchive/dweb-mirror)

### Internet in a Box
Build a platform based on RPI combing a number (TODO list them) of systems

IA next step: Download and attempt to integrate IA server

### Kiwix
(http://www.kiwix.org/) Kiwix is a free app that allows you to search and read Wikipedia without an Internet connection. 
Available for Android, iOS, Windows, macOS and Linux.  
-- from Mike Jensen 2018-11

### KALight
A lightweight version of Khan Academy's educational platform, 
I think this is what runs on Rachel3+ and Internet-in-a-Box ?
- see Learning Equality

### Kolibri
Package and interface for various OER resources, 
Shipped on Internet-in-a-Box (Check) and Rachel3+ (Check)
- see Learning Equality

### Learning Equality 
Non profit developers of Kolibri and KALight 

### LibreMesh
Wifi mesh software (firmware for routers) used by Guidi and Altermundi 

### Mikrotik
Another option that does much the same thing in an integrated hardware/software solution, but quite cheaply, is the MikroTik gear.. 
- from Mike Jensen 2016-03

### Onno Purbo - Indonesia
Is also working on a RPi based educational server - onno@indo.net.id -- from Mike Jensen 2018-11

IA next step: Mitra reached out Dec 2018 with no response. 

### Pfsense
The best option I can think of is Pfsense [https://www.pfsense.org/].  
Runs on little appliances and has built in support for captive portals which can authenticate locally via tiny database or remotely via Radius server.  
Also has loads of other useful tools like bandwidth shaping, firewall, and many other features.  
The UI takes some getting used to in terms of complexity but once it is set up it is pretty bullet-proof.   
It is the sort of thing that could be configured in advance.  
I would run it on something like an Intel NUC. 
- from Steve Song 2016-03-

### PirateBox 
Offline file sharing, on RPi 
[piratebox.cc](https://www.piratebox.cc/doku.php)

Used by autonomous offline networks such as [Fuxico](http://redeautonomafeminista.org/fuxico/)

### Pnkgo
Kit for wifi etc in emergency. Microtik + RPi + Ubiquity. Own disk images. 
[pnkgo.com](http://pnkgo.com/) -- from Mike Jenson 2019-01 

IA next step - reach out and see what is needed to add a server

### Rachel (TODO need link)
Server (~$500) that has more memory/CPU than raspberry pi and integrated access point & battery backup.
Runs three servers currently (Apache-like; Wikipedia/Zim; Khan Academy) could add Archive server.

Use case is schools in Africa with computers but no internet, 
teachers take box into town to unmetered internet connection for it to self-update.

Contact Ed (US East coast ?)

IA Next steps: Have a unit, part way through figuring out installation challenges that included an ancient version of node. 
On hold till after dweb-mirror v0.1.0 ships.

### Rhizomatic (TODO need link)
Working with indigenous villages, running LTE based nodes with high bandwidth (~50MB/s ?) in village and smaller backhaul (5MB/s ?).
Potential to run servers in village but I don't believe they currently are. Contacts Peter & Maka in Mexico. 

IA Next step: (Mitra & Maka) proposed workshop for IFF.

### SolarSpell
 - Library powered by Raspberry Pi, with Wifi access point http://solarspell.org/ -- from Mike Jensen 2018-11

### Widernet https://www.widernet.org/
 - from Mike Jensen 2019-01-04

### Yunohost
Flexible solutions (for package management) ( like http://yunohost.org/ for example ) with proper training ... - from Nico 2018-12


## Research and other publications

In  developing  countries,  many  would-be  mobile  internet users    perceive    downloadable    video    content    as    too expensive. 
Aggressively degrading this video could reduce its file size and therefore its cost. 
The studies presented here explore  extreme  cases  of  this  quality/cost  trade-off  for mobile  phone  users  in  urban  India.  
A  series  of  online studies tested the effects of manipulating a video’s content, bit rate, frame rate, and audio quality on quality ratings and enjoyment.  
Results  show  that  video  quality  and  thus  file size can be greatly reduced with relatively little decrease in these outcomes. 
A field experiment with low-income users in urban India explored consumers’ choices when presented with  a  trade-off  between  video  quantity  and  quality  
and found  that  nearly  one-third  selected  a  lower  quality  video for the benefit of more video  content. 
Results suggest that offering   lower-quality   videos   to   bandwidth-constrained users  could  provide  monetary  savings  with  
only  minimal reduction in consumer satisfaction. 
[https://www.microsoft.com/en-us/research/wp-content/uploads/2012/10/Oeldorf-Hirsch-NordiCHI2012-LowQualityMobileVideo.pdf]
-- from Mike Jensen 2018-11


## Contact Info for people mentioned here. 
Please feel free to add public contact info if you are contributing above. Please don't put non-public contact info for anyone other than yourself here.
                                                                           

* Mitra Ardron @ Internet Archive - personal: [www.mitra.biz](https://www.mitra.biz) work: [dweb.archive.org](https://dweb.archive.org) repos: github.com/internetarchive/dweb* mitra@mitra.biz
* Nico Pace @ Altermundi
* Mike Jensen @ APC
