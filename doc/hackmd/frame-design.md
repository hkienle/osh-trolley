[![hackmd-github-sync-badge](https://hackmd.io/vnldW8TBSnO_LEm4tbxbGQ/badge)](https://hackmd.io/vnldW8TBSnO_LEm4tbxbGQ)

# `frame-design`
:::info
(c) Holger Kienle  
License (if not stated otherwise below):
[CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
:::

## TLDR Parts
- `beam` (11x):
![](https://img.shields.io/badge/2x-leg--front-light.svg)
![](https://img.shields.io/badge/2x-leg--back-light.svg)
![](https://img.shields.io/badge/2x-platform--side-light.svg)
![](https://img.shields.io/badge/1x-platform--top--back-light.svg)
![](https://img.shields.io/badge/1x-platform--top--front-light.svg)
![](https://img.shields.io/badge/1x-handle-light.svg)
![](https://img.shields.io/badge/2x-handle--joint-light.svg)
- :owl: recommended: `s`=17..22mm (`frame-17x17`..`frame22x22`)
---
- `beam`, optional:
![](https://img.shields.io/badge/1x-platform--top--middle-lightblue.svg)
![](https://img.shields.io/badge/1x-bag__support-lightblue.svg)
- `board`, optional:
![](https://img.shields.io/badge/1x-platform-lightblue.svg)
---
- `fastener-mX`: `nut-mX` `bolt-mX` `washer-mX`
- :owl: recommended: M4 (`fastener-m4`), M5 (`fastener-m5`), M6 (`fastener-m6`)

## Basic structure of the Gridbeam frame

[Gridbeam](@hkienl/diy-gridbeam) is a modular building system that originated in the 1970s, which enables easy assembly with minimal tools.

The frame is assembled from
- `beam`: Gridbeam *beams*
- `fastener-mX`: Metric (DIN/ISO) machine-type fasteners

### Beams (`beam`)
![image](https://hackmd.io/_uploads/Sy6XRz2jgg.png =x200)  
*Single beam with full hole pattern, AI generated*

Beams have a hole-pattern. A true Gridbeam beam has all holes drilled (for maximum re-configuration) and only few holes are used for an actual design. The beams in this project have *reduced hole patterns* where all/most holes are used.

The diameter of the holes match the bolts' diameter (`mX`).

#### Beam profile

The profile of a beam is a square with sides of `SxS` (in mm), for example `17x17` for a 17mm square.
```
       S=17mm
    ←─────────→
    ┌─────────┐  ↑
    │         │  │
    │         │  │
    │         │  │ S=17mm
    │         │  │
    └─────────┘  ↓
```
The short-form for`SxS` is `s`.

#### A beam is made up of segments

A beam can be thought of as a string of individual segments. Each segment has length `s`. The shortest beam has 1 segment, resulting in a cube (SxSxS).
```
              _________
             /        /|
            /        / |
           /________/  |
          |        |   |
  S=17mm  |        |   |
          |        |  /  1 segment of 17mm
          |________|/
          
           S=17mm
```
Strictly speaking, this "deteriorated" beam is not an offical Gridbeam beam. 

A true Gridbeam beam has 2 or more segments.
```
   ___________________
  /        /        /|
 /        /        / |
/________/________/  |
|        |        |  |
|        |        | /  2 segment of 17mm each
|________|________|/
```

:::success
:bulb::straight_ruler: The size of beam can be specified by giving
  1. `s` (e.g. `s`=17mm)
  2. `N`: number of segments (e.g., 2)
For the example, the beam has dimensions 17x17x34mm.
:::

### Tri-joints
![image](https://hackmd.io/_uploads/HkxG_Qnjex.png =x200)  
*3 beams connected with a tri-joint,
(c) Gridbeamers [:link:](https://www.cnet.com/tech/tech-industry/after-more-than-30-years-grid-beam-modular-construction-system-comes-to-market/)*

Beams are connected with fasteners via Gridbeam-style *tri-joints* ("3D") and (optionally) with "2D"-joints.

The stability and right-angles of the frame are derived from the 3D/tri-joints.

## Fasteners (`fastener-mX`)

### Spec
- `fastener-mX`
    - :exclamation: do not mix `mX`
    - `screw-mX` [DIN 912 cylinder head screw](/@hkienle/std-din-912) (:de: Zylinderkopfschraube)
        - Length (`screw-mX-height`): >= `s`+2*`washer-mX-height`+`nut-mX-height`
    - `nut-mX` [DIN 934 hexagon nut](/@hkienle/std-din-934)  
      | `nut-mX-flat` [DIN 439 low profile hexagon nut](/@hkienle/std-din-934)
    - `washer-mX`
        - :monkey: OK, but discouraged: DIN 912 (both form A and B)
            - too flimsy, both OD and height
        - `washer-mX-dia`
        - :owl: recommended: OD of washer as near as possible to `s`(e.g., 16mm)
        - :exclamation: OD of washer <= `s`
### Notes for spec
- `L`: It may not be possible to select a screw length `L` that perfectly matches the suggested length.
    - Decide whether to got a bit shorter or longer.
        - If you go a **bit shorter**, tightening the nut may squish the material and you end up with a perfect length.
    - If you go a **bit longer**, it may open up the possibility to have 2 nuts at the end (for secure locking).
    - If the screw is **too long** it has an unpleasant esthetics and the user may scratch themselves when handling the frame.
- `washer-mX-dia`: The softer the wood, the more important becomes a washer with larger OD to better distribute the load and to not dent/squish the beams when tightening the nut.

## Matching beams with fasteners

The diameter/strength of the machine screws must match the sturdiness of the beams (parameter `s`).

:::success
:straight_ruler::+1: As a rule of thumb, at the very least, the "meat" around a hole should be the diameter of hole. If the fastener is M4 (hole diamter: 4mm) then  
`s` >= 4(meat)+4(hole)+4(meat)=12mm
:::

For example, for `s`=17mm, both M4 (`fastener-m4`) or M5 (`fastener-m5`) is an appropriate choice.

For the structural stability of a trolley (with a load of max. 20kg) **M6 is sufficient.** (For course, larger is also fine if you have larger screws at hand or prefer the bulky esthetics of larger screws.)

## Trolley frame

The design of the frame is primarily determined by the 
beam profile (`s`), the length of the individual beams (`N`), and how they are connected to each other.

Since `s` is the starting point for dimensioning and procurement, a particular frame instantiation is denoted as `frame-SxS` (e.g., `frame-17x17`).

:::success
:bulb: The way the beams are connected to each other to form the frame is independent of `s`.
:::

:::success
:straight_ruler::+1: For sufficient strength that balances weight and asthetics, `s` is between 13mm and 25mm. The lower end pushes the sturdiness/strength of the design and you should consider to counter this with better material properties (e.g., harder wood instead of cheap softwood, see [frame-material](/@hkienle/frame-material/)).
:::

### Frame design in [interactive viewer](/dN2oN1qmT-ytX0R6rDyE1Q#Browser-based-construction-Gridbeam-CAD) ("Gridbeam CAD")

Note that each beam has the maximum hole patterns (as required by [Gridbeam proper](https://mammouth.ai/shared/cd22ff1b-0ad2-42a8-a92d-8094b98fab4a)). Counting holes helps grokking the design.

<iframe width="100%" height="500" src="https://play.gridbeam.xyz/#1bc8xDoAgDIXhZ4NCGofK1MEQNldHTmG8_2kkiAzC-uVPX8rewS8OEpQVEScS82teoGsxSht_XVRTzKSjGg86kV1RO9vMdAahbpeGu-h2p2z3r7P5j6vem1tHzfLtBw" frameborder="0"></iframe>

*The above frame is interactive! (Please do not destroy the design, you have all the power :muscle::grin:)*

Source: https://play.gridbeam.xyz/#1bc8xDoAgDIXhZ4NCGofK1MEQNldHTmG8_2kkiAzC-uVPX8rewS8OEpQVEScS82teoGsxSht_XVRTzKSjGg86kV1RO9vMdAahbpeGu-h2p2z3r7P5j6vem1tHzfLtBw

#### Screenshots from interactive viewer

##### Complete frame
- Without optional beam 
![](https://img.shields.io/badge/1x-bag__support-lightblue.svg),
which sits below the handle and provides attachment for the bag.

![2025-04-15_16-27-05_screenshot](https://hackmd.io/_uploads/rkJoMHVixx.png)

##### Detail of frame's base
- Without optional beam
![](https://img.shields.io/badge/1x-platform--top--middle-lightblue.svg).


![2025-04-17_16-34-29_screenshot](https://hackmd.io/_uploads/SkGbmHEsxe.png)

### Prototype
See [frame-proto](@hkienle/frame-proto/).
