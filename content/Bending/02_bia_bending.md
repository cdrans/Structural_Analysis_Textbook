# Biaxial Bending 
In deriving the Flexure Formula for Symmetric Bending, a number of major assumptions about the beam geometry and loading were made. These assumptions greatly simplified the derivation of the formula; however, they also limit the general applicability of the resulting formula. We will systematically relax some of these assumptions in order to obtain more generalized formulas for bending of beams.

We will start by relaxing the constraint on the orientation of the internal bending moment. Previously, we considered only a bending moment that acted orthogonal to an axis of symmetry of the cross section. In this way, bending deformation was confined to the plane defined by this axis of symmetry and the axis of the beam itself (the $z$-axis). We will now consider the case of the internal moment being oriented by an angle $\theta$ with respect to the axis of symmetry as illustrated in {numref}`Fig:Morient`.
```{figure} figures/Biaxial_Bending.svg
---
width: 80%
name: Fig:Morient
---
Orientation of a moment, $M$, in the $xy$-plane.
```
Take a moment and think about how you would expect the beam to deform under this new internal loading. 
- Where would you expect the neutral axis to be located? 
- Where do you expect the maximum bending stresses to occur? 

Write down your thoughts so that you can critically reflect on them and align your intuition with the resulting theory. Please do not skip this step as it is vital for developing your own engineer intuition.

### Analyzing Biaxial Bending Using Superposition
This loading state of an arbitrary internal bending moment acting within a symmetric beam cross section is typically referred to as *biaxial bending* as it can be viewed as superposition of two symmetric bending problems.  
```{figure} figures/Biaxial_Bending_decomp.svg
---
width: 90%
name: Fig:BiaxBendSup
---
Decomposition of an arbitrary bending moment into a biaxial moment state.
```
Here the moment, $M$, is decomposed into components $M\cos\theta$ and $M\sin\theta$ that can be treated with the symmetric bending equation. Applying the symmetric bending equation for each moment component, we obtain:
```{math}
---
name: eq:BiaxialBend
---
{\sigma _z} = \frac{{{M_x}y}}{{{I_{xx}}}} + \frac{{{M_y}x}}{{{I_{yy}}}}
```
where $M_x$ and $M_y$ are the $x$- and $y$-components of an arbitrary moment $M$, $x$ and $y$ are the distances from the $y$ and $x$ axes respectively, and $I_{xx}$ and $I_{yy}$ are the moments of inertia about the $x$ and $y$ axes respectively. For the above illustrated case, $ {M_x} = M\cos \theta $ as this component produces a positive normal stress in the positive $y$-direction and ${M_y} =  - M\sin \theta $ as this component produces a negative normal stress in the positive $x$-direction.

When analyzing a biaxial bending problem, one must take care when identifying the location of the neutral axis. It may be tempting to think that it will be aligned with moment $M$ as it is with the symmetric bending components, but this is generally not the case. Recognizing that the normal stress at the neutral axis is zero, we can prove this by setting eqn. {eq}`eq:BiaxialBend` equal to zero:

$${\sigma _z} = \frac{{{M_x}y}}{{{I_{xx}}}} + \frac{{{M_y}x}}{{{I_{yy}}}} = 0$$

and then rearranging it define the linear relationship between the $x$ and the $y$ coordinate of the neutral axis:
```{math}
---
name: eq:BiaBendNA
---
\frac{y}{x} =  - \frac{{{M_y}{I_{xx}}}}{{{M_x}{I_{yy}}}} = \tan\alpha 
```
Finally, we can recognize that the ratio of $y/x$ will be equal to the tangent of the angle $\alpha$ as defined in {numref}`Fig:BiaxBendNA`, allowing us to solve for the angle of the neutral axis.
```{figure} figures/Biaxial_bending_NA.svg
---
width: 70%
name: Fig:BiaxBendNA
---
Orientation of the moment and neutral axis in biaxial bending.
```
If we consider a moment $M$ as shown above, we see that eqn. {eq}`eq:BiaBendNA` equation reduces too:

$$\tan \alpha  =  - \frac{{( - M\sin \theta ){I_{xx}}}}{{(M\cos \theta ){I_{yy}}}} = \tan \theta \frac{{{I_{xx}}}}{{{I_{yy}}}}$$

Please note that in the above equation, $M_y$ decomposes into $\left( { - M\sin \theta } \right)$ due to the fact that it produces a negative internal normal stress in the positive $x$-direction.

Here, we can clearly see that the angle of the moment and the neutral axis will only align when the moments of inertia along the $x$ and $y$ axes are the same, which is generally not true. It is also possible to make some additional observations regarding the neutral axis location. Since the moments of inertia have to both be positive quantities, the tangent of angles $\theta$ and $\alpha$ have to have the same sign. This effectively means that the **neutral axis has to pass through the same quadrant of the beam cross section that the resultant moment is pointing**.

For analyzing beam deflections, the same approach can be taken. By decomposing the internal moment into two symmetrical bending cases, the Moment-Curvature Relationship derived in the previous section can be applied to each of these cases and the total deflection obtained by superposition. Be conscious, however, that the bending deflections will be in different directions, so you will need to perform vector addition rather than scalar addition when adding them together.