# `bag_platform` Support platform for the shopping bag
:::info
(c) Holger Kienle  
License (if not stated otherwise below): [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
:::

![image](https://hackmd.io/_uploads/ryXYCJTTxe.png =x300)  
*Example board (MDF, 10mm, scrap) used in `frame-build-sturdy_cots`*

:construction: 

## Design

### Spec
- Width ("x"): Same as ![](https://img.shields.io/badge/platform--top--back-light.svg)-beam
- Depth ("y"): ![](https://img.shields.io/badge/platform--side-light.svg)-beam - `s`
- Thickness ("z"): Between 10mm .. `s`
    - A thickness that matches `s` may result in a nice, uniform look of the frame (if `s` is not too large).
    - A thickness less than 10mm may look flimsy. MDF should be sturdy enough with 10mm thickness, multiplex for sure.
- Holes/fasteners should match the fasteners of the frame, but in principle a different size or even wood screws could be used.
- Material: any
    - :owl: Recommended: MDF (thicker) or multiplex (thinner).
    - :rocket: Laminate or stack **Correx** sheets crosswise (3-5 layers).

## Procurement (`buy`)
- Buy from hardware store or scavenge.

## Manufacture (`mfg`)

### Cutting
- A hardware store will cut the size for you.
- Otherwise, select the cutting tool that properly matches the material.

### Drilling
- If the drill distance determined via offsets from the edges of the board, it is important that be board is cut according to spec.
- The beams ![](https://img.shields.io/badge/1x-platform--top--back-light.svg) and ![](https://img.shields.io/badge/1x-platform--top--front-light.svg) have to be drilled to match the holes in the board (2 holes each).

#### Drill pattern

```
   1 2 3 ... 3 2 1     o: hole to drill
  +---------------+
1 |    o     o    |    platform-top-back
2 |               |
  ⋮              ⋮
2 |               |
1 |o             o|    platform-top-front
  +---------------+
   1 2 3 ... 3 2 1
```

### Mounting

![image](https://hackmd.io/_uploads/S12xkeaalg.png =x200)
*The board is fixated with 4 screws throught the board's holes*

- The platform is fixated to the ![](https://img.shields.io/badge/1x-platform--top--back-light.svg) and ![](https://img.shields.io/badge/1x-platform--top--front-light.svg) beams.
    - ![image](https://hackmd.io/_uploads/r15NJlpplx.png =x200)
*The board sits on top of the tri-joint screws of these beam*


