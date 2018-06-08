# Awesome Plotters [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome) [![Build Status](https://travis-ci.org/beardicus/awesome-plotters.svg)](https://travis-ci.org/beardicus/awesome-plotters)

A curated list of code and resources for pen plotters and other robots that draw.

## Contributing

Contributions are very welcome. Please see [CONTRIBUTING](CONTRIBUTING.md) and [CODE-OF-CONDUCT](CODE-OF-CONDUCT.md) for details.

## Contents

* [Hardware](#hardware)
  * [Plotters](#plotters)
  * [Motor Controllers](#motor-controllers)
  * [Accessories](#accessories)
  * [Pens](#pens)
* [Software](#software)
  * [HPGL](#hpgl)
  * [G-code](#g-code)
  * [Plotter-Specific](#plotter-specific)
  * [Vector Creation](#vector-creation)
  * [Vector Utilities](#vector-utilities)
  * [Fonts](#fonts)
* [Inspiration and Instruction](#inspiration-and-instruction)
* [Community](#community)
* [Other Awesomes](#other-awesomes)

## Hardware

### Plotters

* [AxiDraw](https://shop.evilmadscientist.com/productsmenu/846) – pen plotter from [Evil Mad Scientist](https://www.evilmadscientist.com/), very popular on [#plottertwitter](https://twitter.com/hashtag/plottertwitter)
* [Line-us](https://www.line-us.com/) – a cute little kickstarted robotic drawing arm
* [Makeblock XY Plotter](https://makeblockshop.eu/products/makeblock-xy-plotter) – hackable XY plotter kit (possibly discontinued)
* [Drawing Robot](https://www.thingiverse.com/thing:2349232) – 3d-Printable AxiDraw clone w/ [Arduino CNC Shield](https://blog.protoneer.co.nz/arduino-cnc-shield/) controller running grbl firmware
* [WaterColorBot](https://watercolorbot.com/) – XY art robot and software to plot with watercolor paints
* [EggBot](https://egg-bot.com/) – pen plotter for egg-shaped and spherical objects
* [HP Pen Plotters](http://www.hpmuseum.net/exhibit.php?class=4&cat=24) – vintage desktop and floor-standing pen plotters from the creator of the HPGL standard. Model 7475A is very common and can usually be found on eBay
* [Roland Pen Plotters](https://www.youtube.com/watch?v=6_pwzqPk6Gg) (YouTube) – vintage flatbed HPGL pen plotters. Search eBay for "roland dxy"

### Motor Controllers

* [grblShield](https://github.com/synthetos/grblShield) – all the stepper motor control hardware needed to turn an [Arduino](https://www.arduino.cc/) into a G-code-based motion controller using the grbl firmware ([adafruit](https://www.adafruit.com/product/1750))
* [TinyG](https://github.com/synthetos/TinyG/) – more featureful and robust 6-axis G-code-based motion control hardware ([adafruit](https://www.adafruit.com/product/1749))
* [Arduino CNC Shield](https://blog.protoneer.co.nz/arduino-cnc-shield/) – grbl-compatible stepper motor control shield for Arduino, similar to the [grblShield](https://github.com/synthetos/grblShield)
* [Raspberry Pi CNC Hat](https://wiki.protoneer.co.nz/Raspberry_Pi_CNC) – Raspberry Pi add-on board w/ stepper controllers and a microcontroller running grbl. Interfaces with the Pi's serial pins

### Accessories

* [WiFi232](http://biosrhythm.com/?page_id=1453) – wifi to RS-232 serial via a DB25 plug. Control your serial plotter wirelessly
* [Plotter Cable Pinout](http://sites.music.columbia.edu/cmc/chiplotle/plotter_cable.pdf) (PDF) – schematic for a plotter cable that will work for most HP and Roland plotters. Search eBay or Amazon for `DB9 to DB25 Serial Null Modem Cable` or similar to find them for sale

### Pens

* [Sharpie Fine Point Plotter Adapter](https://www.thingiverse.com/thing:229982) – 3d-printed adapter to fit a standard Sharpie in an HP-GL plotter
* [Parametric 3d-Printable Plotter Pen Adapter](https://openjscad.org/#https://gist.githubusercontent.com/beardicus/d668c0f6b96be53d16dc/raw/plotter-pen-adapter.jscad) – adjustable model to print adapters for various pens
* [Plotter Pen STL Models](https://www.thingiverse.com/thing:227985) – accurate STL models of both short and long standard plotter pens
* TODO: pen recommendations

## Software

### HPGL

HPGL is a serial/text-based protocol used by most old pen plotters, and even many new vinyl cutters.

* [Chiplotle](https://github.com/drepetto/chiplotle) ([web site](http://chiplotle.org/)) – Python library for generating HPGL and interfacing with serial plotters
* [HPGL Reference Guide](http://www.isoplotec.co.jp/HPGL/eHPGL.htm) – HTML-based HPGL Reference
* [HP 7475A Interfacing and Programming Manual](https://archive.org/details/HP7475AInterfacingandProgrammingManual) – scanned PDF manual that contains a full HPGL reference
* [djipco/hpgl](https://github.com/djipco/hpgl) – A Node.js library to communicate with HPGL-compatible plotters and printers
* [hp2xx](https://www.gnu.org/software/hp2xx/) – GNU tool to convert HPGL into other vector and raster formats. Can also be used as a previewing in X11

### G-code

G-code is a text-based standard for controlling CNC machines. Though it was designed for industrial machines, its use in many hobbyist 3d printer firmwares has made it ubiquitous in small-scale DIY projects as well.

* [grbl](https://github.com/grbl/grbl) – a high-performance G-code interpreting firmware for the Atmega 328 microcontroller and Arduino
* [cncjs](https://github.com/cncjs/cncjs) – a web-based interface controlling CNC machines running grbl, TinyG, or other G-code-based firmware
* [node-gcode](https://github.com/ryansturmer/node-gcode) – Node.js-based G-code interpreter and similator
* [svg2gcode](https://github.com/em/svg2gcode) – Node.js-based command line utility for converting SVG to G-code
* [svg2gcode](https://github.com/vishpat/svg2gcode) – Python-based utility for fast SVG to G-code conversion
* [Universal-G-Code-Sender](https://github.com/winder/Universal-G-Code-Sender) – Java-based grbl-compatible cross-platform G-code sender
* [ChiliPeppr Hardware Fiddle](http://chilipeppr.com/) – modular web-based workspaces to visualize G-code and control hardware

### Plotter-Specific

Software that is specific to a particular plotter or controller.

* [axidraw](https://github.com/evil-mad/axidraw) – official AxiDraw extensions for Inkscape
* [axi](https://github.com/fogleman/axi) – unofficial Python library for the AxiDraw v3
* [xy](https://github.com/fogleman/xy) – utilities for the Makeblock XY Plotter Robot Kit
* [LaserGRBL](https://github.com/arkypita/LaserGRBL) – laser-optimized Windows GUI for grbl controllers. Could be repurposed for DIY pen plotters that use a solenoid for pen up/down movements
* [Line-us Inkscape Plugin](https://github.com/Line-us/Inkscape-Plugin) – sends drawings to the [Line-us plotter](https://www.line-us.com/) directly from Inkscape
* [Line-us API Examples](https://github.com/Line-us/Line-us-Programming) – example code for the [Line-us](https://www.line-us.com/) plotter's G-code-based API

### Vector Creation

Tools to create vector artwork from scratch or by conversion from other formats.

* [Inkscape](https://inkscape.org/) – popular cross-platform open source vector graphics editor
* [p5.js](https://p5js.org/) – "javascript library that makes coding accessible for artists, designers, educators, and beginners"
* [Paper.js](http://paperjs.org/) – "The Swiss Army Knife of Vector Graphics Scripting"
* [ln](https://github.com/fogleman/ln) – vector-based 3D renderer written in Go
* [autotrace](https://github.com/autotrace/autotrace) – converts bitmap images to vector graphics
* [stipplegen](https://github.com/evil-mad/stipplegen) – creates intereting stippled drawings from bitmap images ([blog post](https://www.evilmadscientist.com/2012/stipplegen2/))
* [SquiggleDraw](https://github.com/gwygonik/SquiggleDraw/commits/master) – "SquiggleDraw will create a SVG file from an image, using the brightness to change the amplitude of sine waves"
* [svgurt](http://svgurt.com/) – web-based PNG to SVG creative noodler
* [penplot](https://github.com/mattdesl/penplot) – a development environment for plotter art in JavaScript
* [penkit](https://github.com/paulgb/penkit) – a Python library for creating line-based SVG graphics

### Vector Utilities

Tools to manipulate and optimize vector-based file formats.

* [svgsort](https://github.com/inconvergent/svgsort) – path planning for plotting SVG files, reduces time spent moving with the pen up
* [svgo](https://github.com/svg/svgo) – Node.js-based tool for optimizing SVG files
* [penkit-optimize](https://github.com/paulgb/penkit/tree/master/optimizer) – An SVG optimizer that uses a vehical routing solver to minimize plot time.

### Fonts

Single-line vector fonts or "engraving fonts".

* [Hershey Vector Font](http://paulbourke.net/dataformats/hershey/) – `.fnt` format of vector fonts from the 60s. Includes a good overview of the original data format of the fonts
* [hershey-fonts](https://github.com/kamalmostafa/hershey-fonts) – C library and original font data for the Hershey fonts
* [OneLineFonts.com](http://www.onelinefonts.com/) – commercial site with some single-line fonts available for purchase

## Inspiration and Instruction

Blog posts, articles, tutorials, galleries, videos, et cetera.

* [An Intro to Pen Plotters](http://www.tobiastoft.com/posts/an-intro-to-pen-plotters) – good info on getting started with old HPGL plotters
* [1980s pen plotters of the future](https://notes.variogr.am/2012/08/12/1980s-pen-plotters-of-the-future/) – another intro to vintage pen plotters
* [Pen Plotter Programming: The Basics](https://medium.com/@fogleman/pen-plotter-programming-the-basics-ec0407ab5929) – some basics of programming vector paths, including sorting, joining, and simplifying
* [On Generative Algorithms](https://inconvergent.net/generative/) – nice 13-part walkthrough of interesting algorithms
* [Roland DG DXY-990](https://hackaday.io/project/12276-roland-dg-dxy-990) – quickstart guide for a Roland flatbed plotter
* [The Cohen-Sutherland Line Clipping Algorithm](https://sighack.com/post/cohen-sutherland-line-clipping-algorithm) – detailed explanation and examples of an interesting algorithm
* [Vera Molnár](https://www.surfacemag.com/articles/vera-molnar-in-thinking-machines-at-moma/) – OG plotter artist
* [The Recode Project](http://recodeproject.com/) – "The ReCode Project is a community-driven effort to preserve computer art by translating it into a modern programming language"
* [Hektor](http://juerglehni.com/works/hektor) – the original cable-based drawbot from 2002
* [Pen Plotter Art & Algorithms Part I](https://mattdesl.svbtle.com/pen-plotter-1) and [II](https://mattdesl.svbtle.com/pen-plotter-1) – a two-part intro to creating generative graphics for plotting
* [Surface Projection](https://bitaesthetics.com/posts/surface-projection.html) and [Fractal Generation with L-Systems](https://bitaesthetics.com/posts/fractal-generation-with-l-systems.html) – each introduce techniques for creating line graphics suitable for plotting

## Community

Where to find other plotter and drawbot friends.

* [#plottertwitter](https://twitter.com/hashtag/plottertwitter) – Twitter hashtag with lots o' plots
* [PlotterArt Subreddit](https://www.reddit.com/r/PlotterArt/)
* [AxiDraw Subreddit](https://www.reddit.com/r/axidraw/)
* [Generative Art Subreddit](https://www.reddit.com/r/generative/)
* [Chiplotle-discuss](https://lists.columbia.edu/mailman/listinfo/chiplotle-discuss) – fairly inactive mailing list for the Chiplotle HPGL Python library with some general plotter talk

## Other Awesomes

* [awesome-generative-art](https://github.com/kosmos/awesome-generative-art)
* [awesome-creative-coding](https://github.com/terkelg/awesome-creative-coding)
