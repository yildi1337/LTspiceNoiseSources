# LTspiceNoiseSources
White and Flicker Noise Sources for LTspice

# Introduction
With the `.noise` command LTspice is able to perform noise analyses while considering e.g. thermal noise of resistors and noise of models provided by semiconductor manufacturers. However, LTspice's library does not contain models of simple voltage and current noise sources. Based on a blog entry from [Axotron](http://axotron.se/blog/voltage-and-current-noise-sources-in-ltspice-noise-simulations/), an extension for the LTspice library is offered here that includes an easy to include and easy to use voltage and current noise source. In both cases white noise ($f^0$) as well as flicker noise ($f^{-1}$) can be defined. $`a^2+b^2=c^2`$

The **voltage noise source (Vn)** has three parameters where `white` defines the ($f^0$) white voltage noise and `flicker` defines the ($f^{-1}$) flicker voltage noise, both in units of $\mathrm{V}/\sqrt{\mathrm{Hz}}$. Due to the frequency-dependent nature of flicker noise, a third parameter `flickerfreq` exists that defines the frequency (in Hz) at which the flicker voltage noise defined according to `flicker` applies. For frequencies below and above `flickerfreq`, respectively, the flicker voltage noise progresses with $-10~\mathrm{dB}/\mathrm{decade}$.
<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/info/info_vnoise.png" />
</p>

The **current noise source (In)** has three parameters where `white` defines the ($f^0$) white current noise and `flicker` defines the ($f^{-1}$) flicker current noise, both in units of $\mathrm{A}/\sqrt{\mathrm{Hz}}$. Due to the frequency-dependent nature of flicker noise, a third parameter `flickerfreq` exists that defines the frequency (in Hz) at which the flicker current noise defined according to `flicker` applies. For frequencies below and above `flickerfreq`, respectively, the flicker current noise progresses with $-10~\mathrm{dB}/\mathrm{decade}$.
<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/info/info_inoise.png" />
</p>

# Examples
The following two screenshots demonstrate the operation of an embedded voltage noise source (top) and an embedded current noise source (bottom).

<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/examples/example_vnoise.png" />
</p>

<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/examples/example_inoise.png" />
</p>

# Usage
To be able to use the noise sources, only the four files

* vnoise.asy (symbol)
* vnoise.sub (netlist)
* inoise.asy (symbol)
* inoise.sub (netlist)

from the `lib` subdirectory have to be copied into the directory of the actual simulation. You can simply download the [examples.zip](https://github.com/yildi1337/LTspiceNoiseSources/blob/main/examples/examples.zip) archive which contains two simulation examples together with the required lib files.

# Implementation Details
The actual implementation of the two noise sources can be seen in the two figures below. Further details can be found in a blog entry by [Axotron](http://axotron.se/blog/voltage-and-current-noise-sources-in-ltspice-noise-simulations/).

**Voltage noise source:**
<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/lib/vnoise.png" />
</p>

**Current noise source:**
<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/lib/inoise.png" />
</p>
