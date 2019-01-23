# Captive Portal requirements

From a conversation with Bruno there seems to be a common need for an Open Source captive portal that works for the
remote networks community. 

## Needs identification

* Independence of the exact choices made by different teams, i.e. this is not "Internet in A Box" or "Rachel", 
* Independence from hardware - e.g. RPi, Rachel-3
* Support for requirements relatively unique to community networking e.g. Mesh
* Allows for at least three tiers of usage 
  * Free material - typically local e.g. health info provided by a government health department sponsor
  * Locally held premium material - e.g. movies, which incur the network a cost to download, but can not to distribute multiple times. 
    Typically this might be a small monthly fee.
  * Access to the net itself - typically billed by bandwidth
  * but note any network may not use all of these.
* Can track (and therefore ration or charge for) bandwidth used locally and over backhaul. 
* Does not depend on SaaS on backhaul for operation.

## PAYG

PAYG has made great strides in bringing access to energy, 
but is (to our knowledge) little used in community networks. 

Given the local management of these systems, and the cost/complexity of mobile money integration, 
a token system would probably work best. 

A rough design might be ....
* Administrator privilige can be used to acknowledge a payment from an agent (e.g. local kiosk owner) and gives them a balance. 
* Kiosk owner sells access to end users either to pay a monthly fee for access to local content or bandwidth. 

## Solutions that get close ... 

What is there that has some of this, and which bits are missing. 

* Please add examples here.
