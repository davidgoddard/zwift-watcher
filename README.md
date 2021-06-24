# Zwift watcher

## Overview

This is single standalone web page that demonstrates a way to read the gradient information off the Zwift screen.  The code supports sending this information via web sockets to a microcontroller to do the actual bike lifting.

This is offered as is and is not a complete or finished product.

## To use

Start Zwift.

Download the zwift-watcher file to your PC and then drag the file to your web browser to open it - I developed on Chrome in case you encounter issues with other browsers.

With the page open simply click on the "Start Watching" button and use the pop-up dialogue to find and share you Zwift screen.

If the gradient is already being shown it should locate it and start showing in large digits the detected value.  If it does not detect it you can click the "Rescan for ROI" button (Region of interest) to try to locate it.  A small rectangle shows the detected area.  

A smaller value in red shows the some measure of certainty of the match.  The process tries to mask out the digits from the background and compare them to the ones in its library.  But screen resolutions and the background colours within the picture can result in less than perfect matches - this is normal.

There is code within the page to connect via web sockets to the given IP address (presumed to be a microcontroller also on your wifi network) to which it sends the digits when they change.

## The files

There are two very similar web pages - try both.  They differ by the steps that they use to isolate the image prior to recognition.

There is a lot of code that is in the files left because these files were part of a try-and-see approach where lots of ideas came and went and lots of support was needed to help capture samples with which to build the reference library used by the page.

The training/learning used a small Node-js server hosting a service which would store a guessed at image.  A quick scan by human eye would see where the file name (which was the guessed at number) and the actual image differed. Then external tools were developed to help collate the correct matches and turn them back into the embedded reference library within the web pages.  

