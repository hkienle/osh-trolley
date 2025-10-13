# `frame-13x13` Frame with 13x13 profile
:::info
(c) Holger Kienle  
License (if not stated otherwise): [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
:::

:::success
:book: Study the [generic frame design](/@kienle/frame-design) before this instantiation of the design.
:::

## Preamble
This design purposely pushed the structural limits of the frame. It goes for a sleek, even fragile, aesthetics that wants to challenge the observer and spook the cautious engineer :ghost:.

## :judge: Spec

### Beam profile and fasteners
- `beam`: `s`=13mm
    - See below for individual beams.
- `fastener-mX`: `X`=3|4 (M3 xor M4)
    - :owl: recommended: M4

### Frame dimensions

Note that the frame dimensions differ from trolley's dimensions, mainly because it misses the axle mount.

- `frame-width`: 338mm (corresponds to `beam-26`)
- `frame-depth`: 234mm (corresponds to `beam-18`)
- `frame-height`: 897mm (corresponds to `beam-67`+`beam-2`)

### Beam length
- `beam-N` (11x)
    - :bulb:`N`: To fully specify each beam, it is sufficient to give its length as the number of segments.

For convenience, the beams' length is also given in mm below.

:::warning
Each unique name for a beams denotes a unique hole pattern. Thus, for example ![](https://img.shields.io/badge/1x-handle-light.svg) differs from ![](https://img.shields.io/badge/1x-bag__support-lightblue.svg), even though they have the same lengths.
:::

#### Minimal frame

:exclamation: For structural integrity, all of these beams are mandatory.

- `beam-11`: ![](https://img.shields.io/badge/2x-leg--front-light.svg) Length: 143mm
- `beam-67`: ![](https://img.shields.io/badge/2x-leg--back-light.svg) Length: 871mm (:star: See customization below.)
- `beam-18`: ![](https://img.shields.io/badge/2x-platform--side-light.svg) Length: 234mm
- `beam-26`: ![](https://img.shields.io/badge/1x-platform--top--back-light.svg) ![](https://img.shields.io/badge/1x-platform--top--front-light.svg) ![](https://img.shields.io/badge/1x-handle-light.svg) Length: 338mm
    - Each beam has a unique hole pattern!
- `beam-2`: ![](https://img.shields.io/badge/2x-handle--joint-light.svg) Length: 26mm

#### Optional beams
- `beam-26`: ![](https://img.shields.io/badge/1x-platform--top--middle-lightblue.svg) Length: 338mm
- `beam-26` ![](https://img.shields.io/badge/1x-bag__support-lightblue.svg) Length: 338mm

## :star: Customizations

### Beams ![](https://img.shields.io/badge/2x-leg--back-light.svg)
- These beams determine the height of the handle. Depending on the height of the user it can be adapted. (The default height of 897mm is in the middle of the range.)

## :owl: Advice
- Consider adding the optional beams (even though you may not use ![](https://img.shields.io/badge/1x-bag__support-lightblue.svg) for its intended purpose).
    - Both optional beams can be used to make the structure more stiff by also adding `beam-2` beams for a proper tri-joint connections:
        - ![](https://img.shields.io/badge/1x-bag__support-lightblue.svg) with 2x`beam-2`
        - ![](https://img.shields.io/badge/1x-platform--top--middle-lightblue.svg) with 2x`beam-2`
- Especially when using M3, have washers with large OD to better distribute the load, otherwise softer wood may be easily squished/dented.
- Consider using harder wood (e.g. beech) and/or wood that bends nicely under load (e.g. ash). See [frame-material](/@hkienle/frame-material).
