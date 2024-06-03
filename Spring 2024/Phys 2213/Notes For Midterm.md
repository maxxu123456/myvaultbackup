## Basic Waves
Wave Equation

$\frac{\partial^2 f}{\partial x^2}-\frac{1}{v^2}\frac{\partial^2f}{\partial t^2}=0$
$v=\sqrt{  \frac{\gamma}{m}}$
$v=\frac{\omega}{k}$
$v=\frac{\lambda}{\tau}$
$v=\lambda \nu$
$k=\frac{2\pi}{\lambda}$
$\omega(t)=-\frac{\partial \phi}{\partial t}$
$k(x)=\frac{\partial \phi}{\partial x}$
Phase delay
$\Delta \phi=kd=\omega T$

The electric and magnetic fields are in phase
![[Pasted image 20240217142057.png]]

Intensity
$I=\frac{1}{2}c \epsilon|E|^2$
$I\propto|A|^2$
Where A is the complex amplitutde

Spherical Wave intensity
$E(\vec{r},t)\propto \frac{E_{0}}{r}e^{i(kr-\omega t)}$
$I(r)=\frac{P}{4\pi r^2}\propto \frac{|E_{0}|^2}{r^2}$

## Doppler Effect

Source is moving
$\nu_{-}=\frac{\nu}{1+\frac{v}{c}}$
$\nu_{+}=\frac{\nu}{1-\frac{v}{c}}$

If you are moving
$\nu_{-}=\nu\left( 1-\frac{v}{c} \right)$
$\nu_{+}=\nu\left( 1+\frac{v}{c} \right)$

Damping
![[Pasted image 20240217143248.png]]

Absorption Coeffcieitn $\alpha$
Refractive Index n
![[Pasted image 20240217143441.png]]

Light Wave in Medium
![[Pasted image 20240217143453.png]]

The intensity decreases exponentially. And the wavelength (and k) and the amplitude change, but the frequency $\omega$ doesn't change

## Refraction

This is the bending of light due to light passing through different medium

$n_{1}\sin(\theta_{1})=n_{2}\sin(\theta_{2})$

## Dispersion

Dispersion is the tendency of optical properties to depend on frequency

$n(\lambda)$ where n is a function of lambda



## Absorption Spectrum of Air

$I(z)=I(0)e^{-\alpha z}$

Attenuation = $\frac{I(z)}{I(0)}=e^{-\alpha z}$

## Counter Propagating Waves

![[Pasted image 20240217145050.png]]

## Standing Waves in a Laser

![[Pasted image 20240217145319.png]]


## Boundary Conditions in 2d Problems

![[Pasted image 20240217145347.png]]


## Beams Crossing at an Angle

![[Pasted image 20240217145624.png]]

Fringe Spacing $\Lambda=\frac{\lambda}{2\sin(\theta)}$

## Intentionally Varying the Delay

Time delay = $\frac{2\delta L}{c}$
Phase delay = $\frac{2\omega\delta L}{c}=2k\delta L$

## Fringes in Delay

![[Pasted image 20240217150329.png]]



## Michelson Inferometer

![[Pasted image 20240217150358.png]]
![[Pasted image 20240217150410.png]]

## Abbe Limit

The smallest resolution that a wave can focus at is $\frac{\lambda}{2}$

## Group Velocity

$v_{g}\equiv \frac{d\omega}{dk}$

The group velocity is the velocity of the envelope or irradiance.

The carrier wave propagates at the phase velocity, $v_{\phi}$
And the pulse envelope propagates at the group velocity, $v_g$

$E(t)\propto A_{\text{pulse}}(z-v_{g}t)e^{ik(z-v_{\phi}t)}$
$E(t)\propto \sqrt{ I_{\text{Pulse}} (z-v_{g}t)}e^{ik(z-v_{\phi}t)}$

Most commonly, phase velocity > group velocity

## Diffraction Gratings

$a[\sin(\theta_{m})-\sin(\theta_{i})]=m\lambda$


## Fourier Transform

$F(\omega)=\int_{-\infty}^{\infty} f(t)\exp(-i\omega t) \, dt$

Inverse Fourier transform

$f(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty} F(\omega)\exp(i\omega t) \, d\omega$

Spectrum
$S(\omega)\equiv |F(f(t))|^2$


Fourier transform of of rect(t)

$F(\omega)=\int_{-\frac{1}{2}}^{\frac{1}{2}} \exp(-i\omega t)\, dt$

$F(\omega)=\text{sinc}\left( \frac{\omega}{2} \right)$

Fourier transform of gaussian

$f(t)=\exp(-\frac{t^2}{2})$
$F(\omega)\propto \exp\left( -\frac{\omega ^2}{2} \right)$

### Scale Theorem

$F\left( f\left( \frac{t}{a} \right) \right)=|a|F(a\omega)$

The shorter the pulse, the broader the spectrum

## Effective Pulse Length

$\Delta t_{\text{eff}}\equiv \frac{1}{f(0)}\int_{-\infty}^{\infty} |f(t)| \, dt$

## Uncertainty Principle

$\Delta \omega \Delta t\geq 2\pi$
$\Delta \nu \Delta t\geq 1$

## Shift Theorem

$F(f(t-\tau))=\exp(-i\omega \tau)F(\omega)$


## The Fourier Transform of a Double Pulse

$f(t)=\text{rect}\left( \frac{t+\tau}{T} \right)+\text{rect}\left( \frac{t-\tau}{T} \right)$

We get 
$F(\omega)=T\text{sinc}\left( \frac{\omega T}{2} \right)\exp(i\omega \tau)+T\text{sinc}\left( \frac{\omega T}{2} \right)\exp(-i\omega \tau)$
$F(\omega)=2T\text{sinc}\left( \frac{\omega T}{2} \right)\cos(\omega \tau)$

## Spacial Fourier Transform

![[Pasted image 20240217154405.png]]



## 2D Fourier Transform

![[Pasted image 20240217154422.png]]
![[Pasted image 20240217154446.png]]

## Diffraction

Definition: 1. the process by which a beam of light or other system of waves is spread out as a result of passing through a narrow aperture or across an edge, typically accompanied by interference between the wave forms produced.

Diffraction SOlution

$E(x',y')\propto \iint t(x,y)E(x,y) \frac{\exp(ikr)}{r}\,\,dxdy$
$r=\sqrt{ z^2+(x'-x)^2+(y'-y)^2 }$


Using Approximations, we get

$E(x',y')\propto \iint t(x,y)\exp(-ik\frac{x x'+yy'}{z})\,\,dxdy$

$k_{x}=\frac{kx'}{z},k_{y}=\frac{ky'}{z}$


Finally we get that 
![[Pasted image 20240217155457.png]]

![[Pasted image 20240217155818.png]]

![[Pasted image 20240218152035.png]]
