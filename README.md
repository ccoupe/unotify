# unotify
MicroPythonOS based application for Linux machines - primarily dedicated raspberrypi's with hdmi screens. But it can and should work on larger host machines like OSX and Linux.

Version 1 of this is implemented in serveral projects. ~/Projects/iots/notify, ~/Projects/iot/dpymsg (several variations in there like dpyluma.py) and ~/Projects/iot/tblogin/

This repo will have serveral new features. It will have an http REST server as well as MQTT. It will queue up the incoming messages, up to 5 deep and purge them 5 minutes after arrival. 
The display 'thread' should copy the oldest queue entry and feed it to the display process. The display will format the message to fit the display and handle any scrolling needed.  After a minute, it should get a new message from the queue  (which could be the an older message, if there is one. If not, then the same message as last time. Upto 5 times (5 minutes)
