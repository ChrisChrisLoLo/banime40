The banime40 v3.0 introduces rotary encoders, however, these encoders are not correctly wired to ground, leading them to end up as floating.

To fix the rotary encoders for the banime40 x3.0, you will need to do the following:
- wire the ground of one rotary encoder ground pints to GND
- sever the connection from the right rotary encoder to the reset button

A user has submitted the following image outlining how to wire up the encoder ground pins to GND
![wiring guide](https://raw.githubusercontent.com/ChrisChrisLoLo/banime40/master/docs/images/hotfix.png)

Additionally, to prevent a hard wiring between ground and reset, you will need to sever the original trace from the rotary encoder ground to the reset button.

You can do so by scraping the trace with a hobby knife.

Apologies for this error, this could have been mitigated by:
- Documenting what functionality is untested, no matter how trivial it may be
- Connecting the reset button to the microcontroller via global tags
