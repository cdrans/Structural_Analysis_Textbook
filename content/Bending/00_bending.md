---
numbering:
  title:
    offset: 0
---
# Bending
Beams are one of the most common structural elements in the design toolbox of an engineer, but what is a beam really? Engineers use the term *beam* to refer to structural elements that satisfy two basic conditions:

1. Its primary axis is much larger than its dimensions in the plane normal to this axis (ie: the cross-sectional plane).
2. It is subjected to external loading transverse to the axis of the beam.

With respect to the second point, this can be point forces, distributed forces, or moments, as long as they act (or have a component that acts) transverse to the axis of the beam. This type of loading will generate internal bending moments within the beam. It is important to recognize that such loading can and will generate internal shear forces as well. Indeed, we have seen in the earlier chapter on internal loading that internal shear and bending are related, $\frac{{dM}}{{dz}} = V$. However, for this chapter, we will focus on pure bending and leave the discussion of transverse shear to later chapters.

In this chapter, we will consider three general classifications of bending: [](01_sym_bending), [](02_bia_bending), and [](03_unsym_bending). The former is the most simplistic and easiest case to analyze and understand conceptually, thus we will start with this case and work our way towards the more general case of unsymmetrical bending. First, however, lets consider the general set of assumptions and conditions we will constrain ourselves when considering bending in this chapter.

## Conventions and Assumptions
Although we will be looking at various cases for bending within this chapter, there are some common conventions and assumptions that we will be making that are stated here. 

First, recall the sign convention for internal forces and moments in a beam with an axis parallel to the $z$-coordinate direction illustrated in [](#Fig:SignConv). In this chapter, we will be limiting our viewpoint to the bending moments $M_x$ and $M_y$. Note the directions of $M_x$ and $M_y$ and review the earlier chapter on internal loading for a detailed explanation of the convention used for positive forces and moments. 

```{figure} figures/Sign_convention_forces_disp.svg
:label: Fig:SignConv
:width: 80%
:align: center

Generalized cantilever beam with standard coordinate system and convention for positive internal (green) and external (blue) loading.
```

As mentioned earlier, we will be limiting our view in this chapter to pure bending and thus on the internal bending moments $M_x$ and $M_y$. Please take note of the positive directions of these internal moments in {numref}`Fig:SignConv` and review the chapter on internal forces for a more detailed description of how we defined this convention.

Additionally, we will be making a few assumptions for our analysis. Some of these assumptions will be motivated throughout the chapter, but they are stated here for completeness. 
- The beam is long and slender (length is more than 10 times larger than cross-section dimensions).
- The beam is prismatic (has a constant cross-section) or only a very gradual taper.
- The beam material is and remains linear elastic during loading with no fracture, plasticity, or local buckling instability taking place.
- The Young's Modulus, $E$, defining the linear elastic properties of the material is the same in tension and compression.
- Beam deformations are small relative to the beam geometry.
- Transverse cross-sectional planes within the unloaded beam remain plane (ie: do not warp or distort) during loading.

The assumptions above will apply to all of the cases of bending treated in this chapter. Additional simplifications specific to each case will be highlighted in the appropriate sections of this chapter.
