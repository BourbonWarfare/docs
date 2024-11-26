# Milliradians Theory

{% hint style="danger" %}
WIP (Stockton)
{% endhint %}

### Milliradians

A milliradian, abbreviated as $$mil$$ or $$mrad$$, is an angular unit of measurement, similar to degrees in a circle.\
Its size is derived from the radian (abbreviated as $$rad$$), a standard SI (metric system) unit.

The prefix "_milli-"_ means multiplication by one thousandth $$(0.001)$$, or $$(10^{-3})$$.\
In other words: division by one thousand.

Thus, **one milliradian is one-thousandth of a radian.**

$$
mil=mrad=rad * 10^{-3}=\frac {rad}{1,000}
$$

Conversely, one radian is equal to one thousand milliradians.\


$$
rad=mrad*10^{3}=mil*1,000
$$

So, then... what is a radian?

The full definition of a radian can be found in _The International System of Units (SI), 9th Edition, 2019_:

> The radian is the coherent unit for plane angle. One radian is the angle subtended at the centre of a circle by an arc that is equal in length to the radius.\
> It is also the unit for phase angle. For periodic phenomena, the phase angle increases by $$2\pi~rad$$ in one period.

Basically, this means that:

* One _radian_ is the angle, with its vertex at the center of a circle, subtended by an arc with the same length as the circle's radiu&#x73;_._
* **The angular size of one radian is the same for any size of circle, because the radian arc length is equal to the circle's radius.**\
  This means that radians are _**not**_ defined by any arbitrary value, such as the definition of $$360\degree$$per circle.

<figure><img src="../../../.gitbook/assets/Circle_radians.gif" alt="" width="225"><figcaption><p>This animation by <a href="https://commons.wikimedia.org/wiki/User:LucasVB">Lucas Vieira</a> shows the relation between radians and circles.</p></figcaption></figure>

The number $$\pi$$, or _pi_, is a constant with an approximate value of&#x20;

$$
\pi=3.14159~26535~89793~23846~26433...
$$

and is defined as the ratio of a circle's circumference $$C$$ to its diameter $$d$$:

$$
\pi=\frac{C}{d}
$$

where $$d=2r$$ for circle radius $$r$$, and can be re-arranged as

$$
C=2 \pi r
$$

Therefore, there are $$2\pi$$ radians per circle, since each circumference has the length of $$2\pi$$ radiuses, and each radius corresponds to $$1~rad$$ of angle.

So, then, multiplying $$2\pi$$ by $$1,000$$ and rounding, we can find the number of milliradians in a circle as approximately

$$
(2\pi~rad)*(\frac{10^{3}~mrad}{rad})\approx6,283.185~mrad
$$

_You may notice that this is analogous to finding the circumference of a circle with radius_ $$10^{3}$$_._

{% hint style="danger" %}
Caution: Not all "milliradians" used in equipment are equal.

For simplified practical use, sometimes the number of milliradians per circle is rounded up or down to an integer, whole-number value, causing errors (which may be acceptable, depending on the application).

Most rifle optics with milliradian reticles should use the correct, precise value of $$2,000\pi~mrad$$ (assuming no manufacturing defects).

However, some equipment (specifically compasses, protractors, and some optics/sighting systems) may intentionally use rounded values:\
NATO equipment may use $$6,400~mrad$$ per circle ($$+1.85916\%$$ error).\
Soviet equipment may use $$6,000~mrad$$ per circle ($$-4.50703\%$$ error).

Clearly, the NATO approximation has less error, but in such cases as artillery direction and adjustment, the same "milliradian" standard should be used for all equipment involved.\
For example, if an artillery crew made adjustments based on a $$6,000~mrad$$ (Soviet) system, but calculations were made using the $$6,400~mrad$$ (NATO) system, there would be significant compounded error that could been avoided by using one system or the other.

Whenever possible, verify the precision of your equipment and whether it uses approximate angular values.
{% endhint %}

### Trigonometry

#### Trigonometric Functions

$$
sin(\theta)=\frac{x}{r}=\frac{opposite}{hypotenuse}
$$

$$
cos(\theta)=\frac{y}{r}=\frac{adjacent}{hypotenuse}
$$

$$
tan(\theta)=\frac{sin(\theta)}{cos(\theta)}=\frac{x}{y}=\frac{opposite}{adjacent}
$$

#### Small Angle Approximations

#### Range Estimation Equations
