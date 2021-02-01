---
layout: post
title: 3D Mohr's Circle and Coulomb Stress Change
bdate: February 1, 2021 12:00 AM
author: Harsha S. Bhat
math: true
tags:
  - Theory
hide: false
---

I am basing this on my old notes and _Bhat et al. (2007)_. Contact me for the relevant Matlab codes.

Assume, without loss of any generality, that the co-ordinate system is
aligned with the principal stresses, $$\sigma_1, \sigma_2, \sigma_3$$. Let $$ (n_1,n_2,n_3) $$ be the components 
of a unit vector, normal to a plane, whose basis are the principal stresses. Further, let $$\sigma_1 \ge \sigma_2 \ge \sigma_3$$.

![3D Mohr's circle](/images/posts/mohrsetup.png)
_Geometry_

Then, the normal and shear tractions are given by,

$$
\sigma_n = \sigma_{ij}n_i n_j \\
\tau_n = \sqrt{(\sigma_{ij}n_j)^2 - \sigma_n^2} \\
n_1^2 + n_2^2 + n_3^2 = 1
$$

Note here that $$\tau$$ is the magnitude of the shear traction vector.
The above is a set of linear simultaneous equations in $$ n_1^2, n_2^2 $$ and $$ n_3^2 $$. The 
solution to which is trivial to obtain.

$$
n_1^2 = \dfrac{\tau_n^2 + 
(\sigma_n-\sigma_2)(\sigma_n-\sigma_3)}{(\sigma_1-\sigma_2)(\sigma_1-\sigma_3)} \ge 0 \\
n_2^2 = \dfrac{\tau_n^2 + 
(\sigma_n-\sigma_3)(\sigma_n-\sigma_1)}{(\sigma_2-\sigma_3)(\sigma_2-\sigma_1)} \ge 0 \\
n_3^2 = \dfrac{\tau_n^2 + 
(\sigma_n-\sigma_1)(\sigma_n-\sigma_2)}{(\sigma_3-\sigma_1)(\sigma_3-\sigma_2)} \ge 0 \\
$$

Now note that, $$\sigma_1 \ge \sigma_2 \ge \sigma_3$$. Thus we get,

$$
\tau_n^2 + (\sigma_n-\sigma_2)(\sigma_n-\sigma_3) \ge 0 \\
\tau_n^2 + (\sigma_n-\sigma_3)(\sigma_n-\sigma_1) \le 0 \\
\tau_n^2 + (\sigma_n-\sigma_1)(\sigma_n-\sigma_2) \ge 0 \\
$$

Each of the above equations represents as 2D Mohr's circle when equated to zero. 
For example, $$ \tau^2 + (\sigma_n-\sigma_2)(\sigma_n-\sigma_3)  = 0 $$ represents a
Mohr's circle in 2D whose end points are $$(\sigma_2,\sigma_3)$$. This is the smallest Mohr's circle.
Thus the first equation is true everywhere outside the circle. The second equation is 
true everywhere inside the Mohr's circle whose end points are $$(\sigma_1,\sigma_3)$$. 
This is the largest Mohr's circle. Following these lines of argument we thus can show that, to satisfy all 
of the above equations simultaneously, any point $$(\sigma_n,\tau_n)$$ must lie in the region bounded
by the three circles, the green shaded region below.

![3D Mohr's circle](/images/posts/mohr.png)
_3D Mohr's Circle. Image from [Wikipedia](https://en.wikipedia.org/wiki/Mohr%27s_circle)_

## Coulomb Stress on Fault Planes of Known Orientation

Consider a fault plane $\Sigma$ lying in a 3D space. Let
$x, y$ and $z$ form a right-handed co-ordinate system
where the surface of the earth is in the $x-y$ plane and the
$z$ axis points vertically upwards from the earth's surface. The
strike direction, $\vec{s}$, is chosen along the surface trace of the
fault plane such that the dip, defined below, is $\le 90^{0}$. Let
$\vec{s}$ make an angle of $\phi$ with the $x$ axis (measured
positive for counterclockwise rotation about $z$) and let 
$\gamma$ be the dip of the faulting plane, measured positive for
right-handed rotation about the strike direction (i. e., angle from
earth's surface at right of the strike direction to the fault plane).
The positive strike direction is always chosen such that
$0<\gamma\le90^{0}$. Let $\Sigma^+$ and $\Sigma^-$ to be the positive
and the negative side of the fault plane respectively [Figure A1a];
$\Sigma^-$ is the footwall (or is assigned arbitrarily if $\gamma =
90^{0}$).

Let $\vec{n}$ be the unit normal to the fault plane directed from
$\Sigma^-$ to $\Sigma^+$. This will imply that any traction calculated
with respect to this vector represents the action on the $\Sigma^-$
plane due to the $\Sigma^+$ plane.

![](/images/posts/faultplane.jpg)

Looking at the above figure the $z$ axis component of $\vec{n}$ is
$\cos\gamma$. The component of $\vec{n}$ on the $x-y$ plane is
then $\sin\gamma$. Since this component is perpendicular to $\vec{s}$,
the strike vector, the projections of $\vec{n}$ on the \textbf{x} and
\textbf{y} axes are $\sin\phi\sin\gamma$ and $-\cos\phi\sin\gamma$
respectively. Thus

$$
\begin{equation} \vec{n} =
(\sin\phi\sin\gamma)\hat{i}+(-\cos\phi\sin\gamma)\hat{j}+(\cos\gamma)\
hat{k} \end{equation}
$$

The unit vector acting along the strike direction is then
given by 

$$
\begin{equation} \vec{s} =
(\cos\phi)\hat{i}+(\sin\phi)\hat{j}+(0)\hat{k} \end{equation}
$$

Then the vector acting along the updip direction is simply
given by $\vec{d} = \vec{n}\times\vec{s}$ which is 

$$
\begin{equation}
\vec{d} =
(-\sin\phi\cos\gamma)\hat{i}+(\cos\phi\cos\gamma)\hat{j}+(\sin\gamma)
\hat{k} \end{equation}
$$

The traction acting on the fault plane is then given by
$T_i=\sigma_{ji}n_j$ where $\sigma_{ij}$ are the components of the
stress tensor (tensile positive) in the original $x-y-z$
coordinate system. The normal stress on the fault plane is then given by
$\sigma=T_in_i$.

The maximum shear stress acting on the plane is given by $\tau_{max} =
\sqrt{\tau_{s}^2+\tau_d^2}$ where $\tau_{s} (= T_is_i)$ and $\tau_{d} (=
T_id_i)$ are the shear stresses acting along the strike and the updip
directions respectively. Define rake angle ($\lambda$) as the angle
between the unit slip vector, $\vec{\xi}$, (slip vector $\Delta \vec{u}$
is defined = $\vec{u}^{+}-\vec{u}^{-}$ where $\vec{u}$ is the
displacement vector) and $\vec{s}$, measured positive from the strike
direction to that of $\vec{\xi}$ for counterclockwise rotation about the
$\vec{n}$ direction.

In terms of the rake angle ($\lambda$) the unit slip vector $\vec{\xi}$
is given by $\vec{\xi}=\vec{s}\cos\lambda+\vec{d}\sin\lambda$ and the
shear stress in the slip direction is given by $\tau = T_i\xi_i$.

It is then clear that a rake angle of $0$ or $\pi$ would
result in pure left or right lateral faulting respectively and a rake
angle of $-\pi/2$ or $\pi/2$ would result in pure normal or thrust
faulting respectively.

The Coulomb Stress (CS) is now given by  $CS=\tau+f_{s}\sigma$ where
$f_{s}$ is the static friction coefficient of the fault plane. $\tau$ is
positive when slip occurs in the direction of the unit slip vector and
$\sigma$ is positive when the fault is unclamped.

The above methodology may be used In circumstances for which the fault
plane is given and the geological sense of motion along it is known and
is assumed to be active after stress change.

## Coulomb Stress (CS) on optimal Mohr-Coulomb planes

From Mohr-Coulomb failure theory it is known that for optimally oriented
planes for failure (planeson which CS is maximum) the unit normals make
angles of $\beta = \pm(\pi/4+\varphi/2)$ (where $\tan\varphi=f_{s}$)
with the maximum compressive stress direction, and their line of
intersection aligns with the intermediate principal stress direction.
The slip vectors of the conjugate planes are in the plane comprising the
maximum and minimum compressive stress directions.

![](/images/posts/optimalplanes.jpg)

The shear and normal stresses on these planes are then given
by

$$
\begin{eqnarray} \tau &=& \frac{(\sigma_1-\sigma_3)}{2}\sin2\beta
\nonumber \\ \sigma &=&
\frac{(\sigma_1+\sigma_3)}{2}+\frac{(\sigma_1-\sigma_3)}{2}\cos2\beta
\end{eqnarray}
$$

where $\sigma_1\ge\sigma_2\ge\sigma_3$ are the principal
stresses, and (like $\sigma$) are positive if tensile.

### Application to plane strain in the $x-y$ plane aligned with the earth's surface

#### Case 1: $\sigma_1=\sigma_{zz}$ (least compressive stress normal to the surface). 

This case results in pure thrust faulting and both the conjugate planes are thrust faults. The strike of
the two planes are along $\pm\vec{\nu_2}$ where $\vec{\nu_2}$ is the
eigen-vector corresponding to the intermediate principal stress,
$\sigma_2$. The dip is $\pi/4-\varphi/2$.

#### Case 2: $\sigma_2=\sigma_{zz}$ (least compressive stress parallel to the surface)

This case results in
strike-slip faulting and the conjugate planes strike left laterally and
right laterally. The strike of the two planes makes an angle of
$\pm(\pi/4-\varphi/2)$ with the maximum compressive stress ($\sigma_3$)
direction. The dip is $\pi/2$.

#### Case 3: $\sigma_3=\sigma_{zz}$ (most compressive stress normal to the surface). 

This case results in pure normal
faulting and both the conjugate planes are normal faults. The strike of
the two planes are given by $\pm\vec{\nu_2}$ where $\vec{\nu_2}$ is the
eigen-vector corresponding to the intermediate principal stress,
$\sigma_2$. The dip is $\pi/4+\varphi/2$. 


### Determination of the change in Coulomb Stress ($\Delta$CS) due to an earthquake rupture

#### Case when fault plane and candidate direction of slip is known

Let $\sigma_{ij}^{0}$ be the initial stress state (in the $x-y-z$ system) and
$\Delta\sigma_{ij}$ be the perturbation to the stress-field due to an
earthquake rupture. Then $\Delta CS$ is given by $\Delta CS =
\Delta\tau+f_{s}\Delta\sigma$ where $\Delta\tau$ and $\Delta\sigma$ are
given by $\Delta\tau=\Delta\sigma_{ij}n_i \xi_j$ and $\Delta\sigma =
\Delta\sigma_{ij}n_in_j$. The vectors $\vec{n}$ and $\vec{\xi}$ are
defined in the first section.

#### Case when fault planes are optimally oriented 

We first begin by determining the conjugate failure planes for the total
stress state i.e. for $\sigma_{ij}=\sigma_{ij}^0+\Delta\sigma_{ij}$. Let
$\vec{\nu_1}$ and $\vec{\nu_3}$ be the eigen-vectors associated with the
minimum and maximum principal stresses respectively of the total stress
state. The failure plane normals are then obtained by rotating
$\vec{\nu_3}$ about $\vec{\nu_2}$ by an angle of $\pm(\pi/4+\varphi/2)$.
Let $\vec{n_1}$ and $\vec{n_2}$ be the outward unit normals to the
conjugate planes and $\vec{ \xi_1}$ and $\vec{\xi_2}$ be the unit
vectors in the direction of slip on the $\Sigma^+_{1/2}$ planes
respectively. Then

$$
\begin{eqnarray} \vec{\xi_1} &=& \vec{\nu_3}\cos \ (\pi/4-\varphi/2) +
\vec{\nu_1}\sin \ (\pi/4-\varphi/2)\\ \vec{n_1} &=& -\vec{\nu_3}\cos \
(\pi/4+\varphi/2) + \vec{\nu_1}\sin \ (\pi/4+\varphi/2) \\ \vec{\xi_2}
&=& \vec{\nu_3}\cos \ (\pi/4-\varphi/2) - \vec{\nu_1}\sin \
(\pi/4-\varphi/2)\\ \vec{n_2} &=& -\vec{\nu_3}\cos \ (\pi/4+\varphi/2) -
\vec{\nu_1}\sin \ (\pi/4+\varphi/2) \end{eqnarray}
$$

$\Delta CS$ is then calculated for each of the optimal planes
by $\Delta CS = \Delta\tau+f_{s}\Delta\sigma$ where $\Delta\tau$ and
$\Delta\sigma$ are given by $\Delta\tau=\Delta\sigma_{ij}n_i\xi_j$ and
$\Delta\sigma = \Delta\sigma_{ij}n_in_j$. $n_i$, $\xi_i$ are the
components of the unit normal and unit slip vectors respectively for
each of the optimal planes. The maximum of the two $\Delta CS$ values is
then sometimes identified as the plane more likely to slip due to an
earthquake rupture, although we see no firm basis for that. However,
this is not the only way the change in Coulomb stress on optimal planes
be identified. The different conjugate fault plane orientations can be
determined for stress states both before ($\sigma_{ij}^{0}$) and after
the rupture ($\sigma_{ij}$) and then the Coulomb stress changes can be
evaluated as

$$
\Delta CS = {CS}_{optimal}^{\sigma^{0}+\Delta\sigma}-{CS}_{optimal}^{\sigma^{0}}
$$

This would give a unique value of $\Delta CS$ regardless of the optimal
plane chosen in each of the stress states.