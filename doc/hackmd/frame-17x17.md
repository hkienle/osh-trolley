[![hackmd-github-sync-badge](https://hackmd.io/lQmxAfu7TOy5vR5IXOEQ3w/badge)](https://hackmd.io/lQmxAfu7TOy5vR5IXOEQ3w)
# `frame-17x17` Frame with `s`=17mm
:::info
(c) Holger Kienle  
License (if not stated otherwise): [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
:::

:::success
:book: Study the [generic frame design](/@kienle/frame-design) before this instantiation of the design.
:::

## :judge: Spec

### Beam profile and fasteners
- `beam`: `s`=17mm
    - See below for individual beams.
- `fastener-mX`: `X`=4|5 (M4 xor M5)
    - :owl: recommended: M4

### Frame dimensions
Note that the frame dimensions differ from trolley's dimensions, mainly because it misses the [frame-wheel_mount](/@hkienle/frame-wheel_mount/).
- `frame-width`: 340mm (corresponds to `beam-20`)
- `frame-depth`: 255mm (corresponds to `beam-15`)
- `frame-height`: 901mm (corresponds to `beam-51`+`beam-2`)

### Beam lengths
- `beam-N` (11x)
    - :bulb:`N`: To fully specify each beam, it is sufficient to give its length as the number of segments.

For convenience, the beams' length is also given in mm below.

:::warning
Each unique name for a beams may denote a unique hole pattern. Thus, for example ![](https://img.shields.io/badge/1x-handle-light.svg) differs from ![](https://img.shields.io/badge/1x-bag__support-lightblue.svg), even though they have the same lengths.
:::

#### Minimal frame

:exclamation: For structural integrity, all of these beams are mandatory.

- `beam-9`: ![](https://img.shields.io/badge/2x-leg--front-light.svg) Length: 153mm
- `beam-51`: ![](https://img.shields.io/badge/2x-leg--back-light.svg) Length: 867mm (:star: See customization below)
- `beam-15`: ![](https://img.shields.io/badge/2x-platform--side-light.svg) Length: 255mm
- `beam-20`: ![](https://img.shields.io/badge/1x-platform--top--back-light.svg) ![](https://img.shields.io/badge/1x-platform--top--front-light.svg) ![](https://img.shields.io/badge/1x-handle-light.svg) Length: 340mm
    - Each beam has a unique hole pattern!
- `beam-2`: ![](https://img.shields.io/badge/2x-handle--joint-light.svg) Length: 34mm

#### Optional beams
- `beam-20`: ![](https://img.shields.io/badge/1x-platform--top--middle-lightblue.svg) Length: 340mm
- `beam-20` ![](https://img.shields.io/badge/1x-bag__support-lightblue.svg) Length: 340mm

### Beam hole patterns
```
                   1                   2   5
 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 … 0 1
 . . . . . . ○ ∥ . . . . . . . . . . . . … ○ ∥ leg-back
 . ∥ ○ . . . . . . . . . . . . . . ○ ∥ .       platform-top-front
 ○ ∥ . . . . . . . . . . . . . . . . ∥ ○       platform-top-back
 ○ ∥ . . . . . . . . . . . . . . . . ∥ ○       handle
 ○ ∥ . . . . . . . . . . . . . . . . ∥ ○       platform-top-iddle (OPT)
 ○ ∥ . . . . . . . . . . . . . . . . ∥ ○       bag_support (OPT)
 ○ ∥ . . . . . . . . . . . ∥ ○                 platform-side
 ○ ∥ . . . . . . .                             leg-front
 ○ ∥                                           handle-joint

 ○ horizontal hole
 ∥ vertical hole
 . no hole
```
See [beam-hole_pattern](/@hkienle/beam-hole_pattern) for further explanations.

## :star: Customizations

### Beams ![](https://img.shields.io/badge/2x-leg--back-light.svg)
- These beams determine the height of the handle. Depending on the height of the user it can be adapted. (The default height of 901mm is in the middle of the range.)
