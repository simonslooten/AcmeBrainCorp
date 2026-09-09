---
id: "6b577d1b-77e0-4684-21b7-baaa18354cd6"
title: "Mermaid - Studio"
notebook: "Radio Ideaal Mermaid"
created: "2026-06-13T12:41:24+00:00"
updated: "2026-06-14T09:26:17+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# Mermaid - Studio

flowchart LR
    subgraph Studio1 [Studio 1 - Links]
        direction TB
        Mic1[4x Mic: 1 DJ + 3 Presentatie
<
br/>Dante Preamps] --> Axite1[D
&
R Axite + Extension Unit
<
br/>Dante-kaart]
        CD1[2x CD Spelers] --> Axite1
        TT1[2x Draaitafels] --> Axite1
        Aeron1[Aeron Studio Computer
<
br/>Playout 1] --> Axite1
        Axite1 --> DanteNet[Dante Network Switch
<
br/>Dedicated VLAN]
    end
    subgraph Studio2 [Studio 2 - Rechts]
        direction TB
        Mic2[1x DJ Mic + 1x Presentatie Mic
<
br/>Dante Preamps] --> Axite2[D
&
R Axite + Extension Unit
<
br/>Dante-kaart]
        CD2[2x CD Spelers] --> Axite2
        Rec2[Bandrecorder + Cassetterecorder] --> Axite2
        Aeron2[Aeron Studio Computer
<
br/>Playout 2] --> Axite2
        Axite2 --> DanteNet
    end
    DanteNet --> DanteMatrix[Hoofd Dante Matrix / Router
<
br/>Axite MambaNet + Dante Controller]
    subgraph ZenderSwitch [Aparte Schakel-Matrix]
        direction TB
        SwitchPanel[Eenvoudige Hardware Panelen + Software
<
br/>op meerdere locaties]
        DanteMatrix --> SwitchPanel
    end
    SwitchPanel -->|Studio 1 →| Ideaal[Ideaal Zender]
    SwitchPanel -->|Studio 2 →| Ideaal
    SwitchPanel -->|Playout 1 →| Ideaal
    SwitchPanel -->|Studio 1 →| IdeaalPlus[IdeaalPlus Zender]
    SwitchPanel -->|Studio 2 →| IdeaalPlus
    SwitchPanel -->|Playout 2 →| IdeaalPlus
    style Studio1 fill:#e6f3ff,stroke:#333
    style Studio2 fill:#e6f3ff,stroke:#333
