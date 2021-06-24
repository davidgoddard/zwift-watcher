# Zwift watcher

## Overview

This is single standalone web page that demonstrates a way to read the gradient information off the Zwift screen.  The code supports sending this information via web sockets to a microcontroller to do the actual bike lifting.

## To use

Start Zwift.

Download the zwift-watcher file to your PC and then drag the file to your web browser to open it - I developed on Chrome in case you encounter issues with other browsers.

With the page open simply click on the "Start Watching" button and use the pop-up dialogue to find and share you Zwift screen.

If the gradient is already being shown it should locate it and start showing in large digits the detected value.  A smaller value in red shows the some measure of certainty of the match.  The process tries to mask out the digits from the background and compare them to the ones in its library.  But screen resolutions and the background colours within the picture can result in less than perfect matches - this is normal.


