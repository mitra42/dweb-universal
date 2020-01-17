# Awesome list - Content Access

This is a list of projects and resources relevant to 
the goal of the Internet Archive's Universal Library Access project of
getting content to places where the internet is of low quality 
either through cost, speed, or censorship. 

See also the companion list of [media coverage](./media.md).

## Guides to contributing
It is curated by Mitra, but with additional curation welcome,
and especially please edit your own entry, or send me a replacement
and any other updates, additions & corrections.

The attribution of sources is partly to give credit, but also a hint as to who might have done further research.

Contact info for contributors is at the bottom.
  
Last update: Mitra 2019-02-10

## Categorisation

As engineers we love to categorize and organize things into stacks, 
so here's my completely arbritrary stack.

* Hardware: Physical devices things run on
* Content: Without content there's nothing to look at,
  this includes aggregators like the Internet Archive, or Wikipedia
* Servers/Apps: Usually tied to a specific set of content, or to a content standard
* Platforms: Software that ties together Servers, Hardware management, admin, 
  access etc with some kind of UI
* Package: package of Platform with content and possibly services
* Implementers: Orgs that take the Platforms and install them in some underserved location.
* Internet Access: Getting the local access, and backhaul to the global internet working, 
  includes mesh networking, satellite links, and local nodes etc
* OneOffs: Hybrids of the different layers put together for specific projects/deployments.
* Vertical: Attempts to do all the above in one project.
* Associations: Organizations that don't fit into one specific category

### Summary Table

Org or Project|Categories|Builds on|Type|Notes
---|-------|----|----|-----
Altermundi|Implementers|Libremesh| |Argentina, Mexico remote villages
Asanka|Package| |For Profit ?|
Blupoint|Platform?| | |Audio only
Bibliotechs Sans Frontiers|Platform| |Non profit|
Bluetown|Platform / Implementers| |For Profit|
BRCK|Vertical| |For-profit|
Coolabs|Platform|Ambien, TV boxes|Non-profit ?|
EduAir|Platforms| | |Cameroon formerly Kwiizi
eGranary|Platforms|Windows| |Confusingly also called Internet In A Box
eLimu|Content| | |
Endless|Platform| | | 
Everylayer|Implementers| |For-profit|Aquired by Brck 2018
FreedomBox| | | |
Guifi|Internet|Libremesh| |Catalonia
IEEE Sight|OneOffs|RPi+?| |Tunisia
Imcon|Package| | |
Internet Archive|Content+Server| |Non-profit|
KA Lite|Servers|Khan Academy|project of Learning Equality|
Kolibri|Servers|OER|project of Learning Equality|
Internet in a Box|Platform|RPi; which servers?|Non-profit ?|
Kiwix|Servers|Wikipedia| |App
Kolibri|Servers|OER|
Inveneo|Implementer| |non-profit|Appears to be defunct
Learning Equality|Servers|Kolibri, KA Light|Non profit|Developers of Kolibri & KA Light
Library Box| | | 
Libremesh|Internet| | |WiFi mesh software
Mikrotik|Platform| | |
Offline Internet Consortium|Association| | 
Onno Purbo|Platform|RPI; which services?| |Indonesia
Othernet|Internet Access| | |
Partnership for Public Access| | | 
Pathagar|Server| | | 
Pfsense|Internet Access| | |
PirateBox|Platform|RPi| |Offline (WiFi) file sharing
Pnkgo|Platform|RPi, Microtik, Ubiquity| |Focus on disasters
Rachel|Hardware+Platform|OER2GO, Kolibri, Intel device|Non-profit|
Rhizomatic|Implementers + Internet Access ?|  RPi|
Solarspell|Vertical|RPI|Non Profit, University|
Widernet|See eGranary
Yunonet| | | 

# Organizations and Projects
##### in Alphabetical order

### Altermundi
Building WiFi mesh networks in remote villages (Argentina ?, Mexico). 
Uses [libremesh](https://chef.libremesh.org/) for mesh, RPi for local servers.
Contact: Nico Pace

### Asanka 
It looks like an RPI with some embedded content and a cloud service.
Commercial service I believe. 
https://www.myasanka.com/ 
(Shared on E4C webinar by Bill Grates)

### Bibliotech sans Frontiers [www.bibliosansfrontieres.org](https://www.bibliosansfrontieres.org)
Have their own platform for off grid libraries. 
Contact: Muy Cheng Peich 

### Blupoint 
BluePoint Integrated content delivery through meshwifi/GSM/bluetooth... including offline environments http://bluepoint.org
Audio based; seems like a bit of a closed-system (curated content only) but I might be misreading that,
or there might be specific applications. MikeJ said: It is a UK business, but their strategy, 
and goals of working on feature phones, fm radio is worth noting 
- particularly as I had already planned to talk to you about the potential for audio content delivery.... 
[blupoint.org](https://www.blupoint.org/why-blupoint/)
 -- from Mike Jensen 2018-11

### Bluetown
Village networks - VSat backhaul, local wireless, captive portal.
Local content paid by sponsors (typically government); PAYG for access to internet
Contact: Lene Sjørslev Schulze

### BRCK 
Had a offline schools system based on iPad, believed to be abandoned, acquired EveryLayer in 2018

### Coolabs (TODO need link)
Location: near Sao Paolo? & Spain

A group of hardware hackers / community network folks where they have local / offline services, 
and are experimenting with tv box for serving local content which is cheaper than RPi 
They were tring the [EGGOIGO 'smart tv'](https://xsreviews.co.uk/reviews/egoiggo-s95x-smart-tv-box-review/) which i believe failed
Contacts: Hiure Quiroz (developer) & Bruno

### EduAir (Formerly Kwiizi) from Cameroon - [eduair.org](http://www.eduair.org)
is the concept name to offer a better education via digital with or without the internet. 
Their work focuses on the design of portable and open media libraries in the form of Boxes with solar energy 
giving access to millions of educational content and offering an integrated communication system where 
learners can make video calls within the local network deployed by the Box 
-- from Mike Jensen 2018-11

### eGrannary / Widernet - NC USA
Platform - works on window, also called Internet in a Box, but no obvious relationship. Clif Missan
-- Mike Jenson Jan2019

### eLimu
Educational agency, eLimu, which creates digital educational material in fun formats, including animations, film and puzzles. 
Used in the Kibera Library project (Kenya) 
-- from Mike Jensen 2018-11

### Endless OS
A repacking of linux to app-ify it and make it useful offline. Restricted to their apps (I think).
More info needed. 
https://endlessos.com/
Thanks to Stefan @ Mobisol for the lead

### EveryLayer - [everylayer.com](http://www.everylayer.com) - Kenya
Was providing WiFi based data packages esp in Nairobi, acquired by BRCK in 2018, 
-- contact was Alicia Levine but not responding to email

### FreedomBox

### Guifi - Catalonia
Largest WiFi mesh network - Catalonia - uses Libremesh. 
Mostly not actually meshing, but extending higher bandwidth fixed connections over WiFi to third parties, 
i.e. they have the payment/sharing part working.

### IEEE Sight -- Tunisia
Developed Raspberry Pi operated devices with hard disks that can be updated periodically with relevant content such as Wikipedia pages, 
IEEE Sight seem to be developing one off systems. e.g. For Tunisia by IEEE in Tunisia & SF. 
TED Talks and other educational content from the Internet. 
They are capable of automatically updating content when connected to Wi-Fi or 3G networks.
[1worldconnected.org/wp-content/uploads/2018/02/Project-Tawasol-Tunisia.pdf](Project-Tawasol-Tunisia.pdf)
-- from Mike Jensen 2018-11 but dont have direct contacts to anyone on the project. 

### Imcon International 
Backpack products - main focus seems an SOS backpack for connecting personally when offgrid.
Uses satellite for the backhaul, haven't had any contact but looks seriously expensive. 
https://imconintl.com/product/edu/ - from Mike Jensen 2019-01-04

### Inveneo
Was a pioneer of radio based nets, but appears (2019) to be defunct, Some of the key people founded Everylayer

### Internet Archive - [archive.org](https://archive.org), [dweb-universal](https://github.com/internetarchive/dweb-universal). 
Almost all our content is in the public domain.  
Currently working on a server to enable offline access [dweb-mirror](https://github.com/internetarchive/dweb-mirror)

### Internet in a Box
Build a platform based on RPI combing a number of systems including KALight & Kolibri,

Internet Archive Universal Library will be in next release.

### Kiwix
(http://www.kiwix.org/) Kiwix is a free app that allows you to search and read Wikipedia without an 
Internet connection. 
Available for Android, iOS, Windows, macOS and Linux.  
-- from Mike Jensen 2018-11

### KALight
A lightweight version of Khan Academy's educational platform, 
Ships on IIAB, and on Rachel3+ (check)
- see Learning Equality

### Kolibri
Package and interface for various OER resources, 
Ships on IIAB, and on Rachel3+ (check)
- see Learning Equality

### Learning Equality 
Non profit developers of Kolibri and KALight 

### Library Box - [librarybox.us](http://librarybox.us)
LibraryBox is an open source, portable digital file distribution tool based on inexpensive hardware that 
enables delivery of educational, healthcare, and other vital information to individuals off the grid.
LibraryBox is a digital distribution tool for education, libraries, healthcare, and emergency response. 
Anywhere there is a lack of open internet access, LibraryBox can bridge the gap of information delivery.

### LibreMesh
Wifi mesh software (firmware for routers) used by Guidi and Altermundi 

### Mikrotik
Another option that does much the same thing in an integrated hardware/software solution, but quite cheaply, is the MikroTik gear.. 
- from Mike Jensen 2016-03

### [Offline Internet Consortium](https://widernet.unc.edu/research/offline-internet-consortium/offline-internet-consortium-initiatives/) [offline-internet.org](https://www.offline-internet.org/)
Consortium of groups involved in the space. 
Contact: Jim O'Donnell

### Onno Purbo - Indonesia
Is also working on a RPi based educational server - from Mike Jensen 2018-11 
(not responsive to emails)

### Othernet
Satellite broadcast system, looks super complicated to setup. https://othernet.is/

### Pfsense 
(network security/captive portal 
'The best option I can think of is Pfsense [https://www.pfsense.org/].  
Runs on little appliances and has built in support for captive portals which can authenticate locally via tiny database or remotely via Radius server.  
Also has loads of other useful tools like bandwidth shaping, firewall, and many other features.  
The UI takes some getting used to in terms of complexity but once it is set up it is pretty bullet-proof.   
It is the sort of thing that could be configured in advance.  
I would run it on something like an Intel NUC.' Steve Song 2016-03-

### Pathagar 
Offline book reader
-- from Sameer Vermar

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
Runs three servers currently (Apache-like; Wikipedia/Zim; Khan Academy) 
adding Internet Archive Universal Library server.

Use case is schools in Africa with computers but no internet, teachers take box into town to unmetered internet connection 
for it to self-update.


### Partnership for Public Access
?  via Carlos (wifi) @ APC

### Rhizomatic (TODO need link)
Working with indigenous villages, running LTE based nodes with high bandwidth (~50MB/s ?) in village and smaller backhaul (5MB/s ?).
Potential to run servers in village but I don't believe they currently are. Contacts Peter & Maka in Mexico. 

IA Next step: (Mitra & Maka) proposed workshop for IFF.
Rumie is a non-profit technology organization that uses today’s low-cost technology to bring high-quality, free digital educational content to youth and learners in remote and underserved communities,more

content that is made available for use without the internet.

### Rumie - rumie.org
Rumie tablets are interactive digital libraries pre-loaded with 1000s of educational resources from our 
LearnCloud (LC) platform. The Rumie LC is an online repository of high-quality educational content sourced 
by educators and volunteers worldwide. Users can also upload their own content onto the LearnCloud platform, 
content that is made available for later offline use. 

### SolarSpell
Offline school Library powered by Raspberry Pi, with Wifi access point and Solar panel. 
Vertically integrated (content, software, curation, deployment, training) 
http://solarspell.org/ (from E4C webinar July 2019)

### TEEAL - http://teeal.org
The Essential Electronic Agricultural Library (TEEAL) is a digital collection containing hundreds of research journals for agriculture and related sciences. more

TEEAL has been improving access at institutions with limited Internet time and/or financial resources.  
It is a searchable, offline, digital library which contains mainly agriculturally focused reference journals, 
as well as coverage in related subject areas.  The collection is updated annually, and the base set is 
provided by the TEEAL Project office in Cornell University’s Mann Library. The non-profit digital library 
contains some of the most prestigious, full-text journals that leading publishers have gifted to TEEAL users. 
TEEAL is available to universities, research institutions, governments, extension organizations and other not-for-profit 
institutions in income-eligible countries. TEEAL works hand-in-hand with Research4Life/AGORA in support of 
access to the agriculture and life sciences research literature and capacity building to enhance use of these resources. 

### Widernet 
[widernet.org](https://www.widernet.org/), see eGranaray

### Yunohost
Flexible solutions (for package management) ( like http://yunohost.org/ for example ) with proper training ... - from Nico 2018-12

## Other quick links 
Mesh Networks: [NYC Mesh](https://docs.nycmesh.net); 
[SuDoRoom/People's Open](https://sudoroom.org); 
[FreiFunk](https://wiki.freifunk.net); 
[Guifi](http://guifi.net/) and [paper](https://people.ac.upc.edu/leandro/docs/analysis.pdf);
[Altermundi](http://blog.altermundi.net) 
[LibreMesh](https://libremesh.org/docs)]

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
* Mike Jensen - coordinates the Locnet program at APC.org

