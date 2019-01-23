# Awesome list - Content Access

This is a list of projects and resources relevant to 
the goal of the Dweb-Universal project of
getting content to places where the internet is of low quality 
either through cost, speed, or censorship. 

## Guides to contributing
It is curated by Mitra, but with additional curation welcome,
and especially please edit your own entry, or send me a replacement.

The attribution of sources is partly to give credit, but also a hint as to who might have done further research.

Contact info is at the bottom 
Last update: Mitra 2019-01-15

## Overview

My initial analysis is that there are three groups of players in this space, 
and that the lines are not solid, i.e. groups often work on multiple parts of 
the problem, in part from necessity. 

* Internet Access - getting the bits to hard to reach places, 
includes mesh networking, satellite links, and local nodes etc
* Content aggregation and sources - includes the Archive, Wikipedia, open maps, open education resources.
* Content curation - the people who understand what content is needed where. 

###Summary Table
Org|Sectors|Type|Notes
---|-------|----|-----
Internet Archive|Aggregation|Non-profit|50 Petabytes; tools for aggregation
Rhizomatic|WiFi|?|
Rachel|Nodes+WiFi|Non-profit|Primary and High schools, packaged content

TODO update this summary from list below

# Organizations and Projects

## Internet Access boxes

### Rhizomatic (TODO need link)
Working with indigenous villages, running LTE based nodes with high bandwidth (~50MB/s ?) in village and smaller backhaul (5MB/s ?).
Potential to run servers in village but I don't believe they currently are. Contacts Peter & Maka in Mexico. 

IA Next step: (Mitra & Maka) proposed workshop for IFF.

### Rachel (TODO need link)
Server (~$500) that has more memory/CPU than raspberry pi and integrated access point & battery backup.
Runs three servers currently (Apache-like; Wikipedia/Zim; Khan Academy) could add Archive server.

Use case is schools in Africa with computers but no internet, 
teachers take box into town to unmetered internet connection for it to self-update.

Contact Ed (US East coast ?)

IA Next steps: Have a unit, part way through figuring out installation challenges that included an ancient version of node. 
On hold till after dweb-mirror v0.1.0 ships.

### Coolabs (TODO need link)
Location: near Sao Paolo?

A great group of hardware hackers / community network folks where they have local / offline services, 
and are experimenting with tv box for serving local content which is cheaper than RPi 
They are using the  EGGOIGO 'smart tv' - see https://xsreviews.co.uk/reviews/egoiggo-s95x-smart-tv-box-review/

Contacts: Hiure Quiroz (developer) & Bruno
 
IA next steps: Mitra Scheduling call with Bruno

### Internet in a Box
TODO - fill in notes from call

### Onno Purbo - Indonesia
Is also working on a RPi based educational server - onno@indo.net.id -- from Mike Jensen 2018-11

Mitra reached out Dec 2018 with no response. 

### Pnkgo
Kit for wifi etc in emergency. Microtik + RPi + Ubiquity. Own disk images. 
[pnkgo.com](http://pnkgo.com/) -- from Mike Jenson 2019-01 

IA next step - reach out and see what is needed to add a server

### Random box links not yet researched
* EduAir (Formerly Kwiizi) from Cameroon is the concept name to offer a better education via digital with or without the internet. Their work focuses on the design of portable and open media libraries in the form of Boxes with solar energy giving access to millions of educational content and offering an integrated communication system where learners can make video calls within the local network deployed by the Box http://www.eduair.org -- from Mike Jensen 2018-11
* IEEE Sight in Tunisia developed Raspberry Pi operated devices with hard disks that can be updated periodically with relevant content such as Wikipedia pages, TED Talks and other educational content from the Internet. They are capable of automatically updating content when connected to Wi-Fi or 3G networks.
  1worldconnected.org/wp-content/uploads/2018/02/Project-Tawasol-Tunisia.pdf -- from Mike Jensen 2018-11
* FreedomBox 
* Flexible solutions (for package management) ( like http://yunohost.org/ for example ) with proper training ... - from Nico 2018-12

## Content Aggregation and Sources

### Internet Archive - [archive.org](https://archive.org), [dweb-universal](https://github.com/internetarchive/dweb-universal). 
Almost all our content is in the public domain.  
Currently working on a server to enable offline access [dweb-mirror](https://github.com/internetarchive/dweb-mirror)

### Blupoint 
Audio based; seems like a bit of a closed-system (curated content only) but I might be misreading that,
or there might be specific applications. MikeJ said: It is a UK business, but their strategy, and goals of working on feature phones, fm radio is worth noting - particularly as I had already planned to talk to you about the potential for audio content delivery.... 
[blupoint.org](https://www.blupoint.org/why-blupoint/)
    
## Software for managing routers / captive portals / local content

These are links to some of the tools, that may or may not be being used in the projects above.  These tools are not the focus of this list, but could be useful in the absence of any other list of them.

The best option I can think of is Pfsense (https://www.pfsense.org/).  Runs on little appliances and has built in support for captive portals which can authenticate locally via tiny database or remotely via Radius server.  Also has loads of other useful tools like bandwidth shaping, firewall, and many other features.  The UI takes some getting used to in terms of complexity but once it is set up it is pretty bullet-proof.   It is the sort of thing that could be configured in advance.  I would run it on something like an Intel NUC. - from Steve Song 2016-03-

Another option that does much the same thing in an integrated hardware/software solution, but quite cheaply, is the MikroTik gear.. - from Mike Jensen 2016-03

## Content creation 
#### Random links
* Educational agency, eLimu, which creates digital educational material in fun formats, including animations, film and puzzles. Used in the Kibera Library project (Kenya) -- from Mike Jensen 2018-11

## Unsorted leads to research and integrate above. 

* https://imconintl.com/product/edu/ - from Mike Jensen 2019-01-04
* https://www.widernet.org/ - from Mike Jensen 2019-01-04
* SolarSpell - Library powered by Raspberry Pi, with Wifi access point http://solarspell.org/ -- from Mike Jensen 2018-11
* Kiwix (http://www.kiwix.org/) Kiwix is a free app that allows you to search and read Wikipedia without an Internet connection. Available for Android, iOS, Windows, macOS and Linux.  -- from Mike Jensen 2018-11
* BluePoint Integrated content delivery through meshwifi/GSM/bluetooth... including offline environments http://bluepoint.org -- from Mike Jensen 2018-11
* In  developing  countries,  many  would-be  mobile  internet users    perceive    downloadable    video    content    as    too expensive. Aggressively degrading this video could reduce its file size and therefore its cost. The studies presented here explore  extreme  cases  of  this  quality/cost  trade-off  for mobile  phone  users  in  urban  India.  A  series  of  online studies tested the effects of manipulating a video’s content, bit rate, frame rate, and audio quality on quality ratings and enjoyment.  Results  show  that  video  quality  and  thus  file size can be greatly reduced with relatively little decrease in these outcomes. A field experiment with low-income users in urban India explored consumers’ choices when presented with  a  trade-off  between  video  quantity  and  quality  and found  that  nearly  one-third  selected  a  lower  quality  video for the benefit of more video  content. Results suggest that offering   lower-quality   videos   to   bandwidth-constrained users  could  provide  monetary  savings  with  only  minimal reduction in consumer satisfaction. https://www.microsoft.com/en-us/research/wp-content/uploads/2012/10/Oeldorf-Hirsch-NordiCHI2012-LowQualityMobileVideo.pdf -- from Mike Jensen 2018-11
* Bluetown

## Contact Info for people mentioned here. 
Please feel free to add public contact info if you are contributing above. Please don't put non-public contact info for anyone other than yourself here.
                                                                           

* Mitra Ardron @ Internet Archive - personal: [www.mitra.biz](https://www.mitra.biz) work: [dweb.archive.org](https://dweb.archive.org) repos: github.com/internetarchive/dweb* mitra@mitra.biz
* Nico Pace @ Altermundi
* Mike Jensen @ APC
