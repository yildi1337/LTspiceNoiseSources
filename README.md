# LTspiceNoiseSources
White and Flicker Noise Sources for LTspice

# Introduction
With the `.noise` command LTspice is able to perform noise analyses while considering e.g. thermal noise of resistors and noise of models provided by semiconductor manufacturers. However, LTspice's library does not include models of simple voltage and current noise sources. Based on a blog entry from [Axotron](http://axotron.se/blog/voltage-and-current-noise-sources-in-ltspice-noise-simulations/), here is a supplement for the LTspice library that includes a voltage noise source and a current noise source. In both cases white noise ($f^0$) as well as flicker noise ($f^{-1}$) can be defined.


