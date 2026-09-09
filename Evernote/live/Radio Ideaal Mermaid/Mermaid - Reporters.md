---
id: "74e69ad8-18b1-4ed7-580f-ce8dfc235acf"
title: "Mermaid - Reporters"
notebook: "Radio Ideaal Mermaid"
created: "2026-06-14T09:22:26+00:00"
updated: "2026-06-14T09:25:58+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# Mermaid - Reporters

flowchart
 
TD
    
subgraph
 
Reporters
 
["4x Verslaggevers in het veld"]
        
R1
[Reporter 1\niRig + Mic + Headset]
        
R2
[Reporter 2\niRig + Mic + Headset]
        
R3
[Reporter 3\niRig + Mic + Headset]
        
R4
[Reporter 4\niRig + Mic + Headset]
    
end
    
subgraph
 
Studio
 
["Studio / Techniekruimte"]
        
Bridge
[Tieline Bridge-IT\n4x Reporter verbindingen]
        
VOIP
[VOIP / Telefoon Hybrides\nBuitenlijnen]
        
        
Deck
[Reporter Mixing Deck\nVOIP + Tieline mixer]
        
        
Axite
[D
&
R Axite + Extension\nStudio 1 of 2]
    
end
    
Zender
[Ideaal / IdeaalPlus Zender]
    
%% Flows
    
R1
 
-->
|5G/WiFi + Report-IT|
 
Bridge
    
R2
 
-->
|5G/WiFi + Report-IT|
 
Bridge
    
R3
 
-->
|5G/WiFi + Report-IT|
 
Bridge
    
R4
 
-->
|5G/WiFi + Report-IT|
 
Bridge
    
Bridge
 
-->
|Analog XLR of Dante|
 
Deck
    
VOIP
 
-->
|Analog of Dante|
 
Deck
    
Deck
 
-->
|"Clean Remote Mix\n(1 stereo/mono lijn)"|
 
Axite
    
Axite
 
-->
|Main Mix|
 
Zender
    
%% Styling
    
classDef
 
field
 
fill
:#
e6f3ff
,
stroke
:#1976
d2
    
classDef
 
studio
 
fill
:#
f0f4f8
,
stroke
:#333
    
classDef
 
output
 
fill
:#
e8f5e8
,
stroke
:#2
e7d32
    
class
 
Reporters
 
field
    
class
 
Studio
 
studio
    
class
 
Zender
 
output
