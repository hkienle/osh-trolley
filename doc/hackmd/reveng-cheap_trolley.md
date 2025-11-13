[![hackmd-github-sync-badge](https://hackmd.io/1O0wGYTsTzKEfpzpUm2uEQ/badge)](https://hackmd.io/1O0wGYTsTzKEfpzpUm2uEQ)

# `reveng-cheap_trolley` Reverse engineering of a cheaply produced trolley frame

:::info
(c) Holger Kienle  
License (if not stated otherwise): [CC BY-SA](https://creativecommons.org/licenses/by-sa/4.0/)
:::

[TOC]

![image](https://hackmd.io/_uploads/Hyxg0EQlWl.png =x250)
![image](https://hackmd.io/_uploads/B1-KfHXlWx.png =x250)  
*Left: Abandoned trolley with one wheel off. Right: Similar functional trolley chained to a bike rack.*

The trolley was found abandoned in the front of my apartment unit in Berlin, Germany. A wheel had come off and I suspect it was discarded on the spot.

Interestingly, a few days later I saw a very similar functional model in the same area that was chained to a bike stand (along with a helmet).

The trolleys **bag**s were missing, it would have been interesting to see which materials and techniques were used.

:::info
The intent here is not to perform a thorough "reverse engineering" of the commercial trolley, but rather to point out relevant properties and design decisions, which could inspire our design or are counterexamples.
:::

## Design observations

- :+1: The trolley is **collapsible** for stowing it away. This seems a desirable property since most commercial trolleys have this feature. Our trolley, however, is not collapsible.

![image](https://hackmd.io/_uploads/BJq3xU7e-l.png =x250)  
*Pipes with plastic connectors and rivets. Note the dent in a pipe due to bending.*

The frame is constructed from aluminum/metal **pipes** that are connected with plastic parts and metal rivets.
- Plastic connectors are a useful design approach because they can be manufactured with 3D-printing.
- :cry: Rivets are problematic because:
    - If a rivet comes loose an orginary user is probably not able to replace it.
    - Rivets are only separable in a destructive manner, which may damage the frame. The rivets cannot be reused an are less accessible compared to screws.
- The pipes are relatively lightweight, offering an excellent stiffness/weight trade-off.
- :cry: Two pipe elements are slightly bend with a noticeable notch as a result. This is relatively difficult and time-consuming to produce for a low-budget frame. Perhaps it had to be done to work around a design flaw?  
![image](https://hackmd.io/_uploads/ry74c87gZx.png =x200)  
*Bend pipe, needed to accomodate collapsing of the frame.*

![image](https://hackmd.io/_uploads/B1FtbImg-l.png =x250)
![image](https://hackmd.io/_uploads/Hk1AWI7g-x.png =x250)  
*Axle design: Metal rod with "bulge" and notch.*

The **axle** is a fixed metal rod that is prevent from sliding with a stamped "bulge" on the inner side and a notch on the other side, which accommodates a metal clamp.
- A fixed metal rod is an effective and cheap design. The rod could be threaded to mimic the bulge and notch with screws.
- :+1: The design shows that an axle--as opposed to a shaft--is a feasible design.

![image](https://hackmd.io/_uploads/H1_PzL7ebl.png =x250)
![image](https://hackmd.io/_uploads/ByO6rLml-e.png =x250)
![image](https://hackmd.io/_uploads/H19lOUmeZx.png =x250)  
*Left: Reducter (restricting fitting) between wheel and axle. Middle: Metal spring that slides over axle notch. Right: Wheel cap with spring*

![image](https://hackmd.io/_uploads/H1IjPLQlbg.png =x250)  
*Assembled reducer and spring, which slides into the axle's notch (without wheel and cap).*

The **wheel mount** is accomplished with a plastic reducer piece and a clamp mechanism that prevents the wheel from sliding off the axle.
- This seems a rather involved design, but it accomplishes a relatively sleek industrial look (the cap hides the mechanics) and easy assembly.
- :cry: Undoing the assembly is surprisingly cumbersome because the spring is not easily detached.

![image](https://hackmd.io/_uploads/r15jq8mxWl.png =x250)
![image](https://hackmd.io/_uploads/rkPAcImg-x.png =x250)  
*Wheel from both sides.*

The **wheel** itself feels quite flimsy, very little material has been used. Note that the inner diameter of the wheel is not round, but oval, to accommodate the reducer.

- On the positive side, the wheel is rather sturdy for the material involved.
- :cry: On the negative side, it's unlikely that the wheel last very long.
- :cry: Replacing the wheel with a COTS product is not straightforward because of the reducer piece.

:::danger
:cry: The wheel mount in conjunction with the flimsy wheel seems quite clearly the *defined breaking point* (:de: Sollbruchstelle) of the design as a whole.
:::

## Weight
- ~400g (without bag)

![image](https://hackmd.io/_uploads/Hkw3TL7lZe.png =x250)  
*Measuring the frame with a kitchen scale*

## Images
- Scavenged trolley https://albums.ente.io/?t=23XMazw9Pd#5pdzBkvG6exj7dC2r6dUTMZmkT6YLkHXKDUXdU4hfELP
- Trolley chained to bike rack https://albums.ente.io/?t=hnuZLvRxSZ#CoQxAnbhhc8qrT4UxGTZGVYMQUhjszAQMmng4wkpUTjw