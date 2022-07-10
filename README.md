# LTspiceNoiseSources
White and Flicker Noise Sources for LTspice

# Introduction
With the `.noise` command LTspice is able to perform noise analyses while considering e.g. thermal noise of resistors and noise of models provided by semiconductor manufacturers. However, LTspice's library does not contain models of simple voltage and current noise sources. Based on a blog entry from [Axotron](http://axotron.se/blog/voltage-and-current-noise-sources-in-ltspice-noise-simulations/), an extension for the LTspice library is offered here that includes an easy to include and easy to use voltage and current noise source. In both cases white noise ($f^0$) as well as flicker noise ($f^{-1}$) can be defined.

The **voltage noise source (Vn)** has three parameters where `white` defines the ($f^0$) white voltage noise and `flicker` defines the ($f^{-1}$) flicker voltage noise, both in units of $\mathrm{V}/\sqrt{\mathrm{Hz}}$. Due to the frequency-dependent nature of flicker noise, a third parameter `flickerfreq` exists that defines the frequency in units of Hz at which the flicker voltage noise defined according to `flicker` applies. For frequencies below and above `flickerfreq`, respectively, the flicker voltage noise progresses with $-10~\mathrm{dB}/\mathrm{decade}$.
<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/info/info_vnoise.png" />
</p>



<p align="center">
  <img src="https://github.com/yildi1337/LTspiceNoiseSources/blob/main/info/info_inoise.png" />
</p>

# 
