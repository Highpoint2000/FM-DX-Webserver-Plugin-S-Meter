# S-Meter plugin for FM-DX-Webserver

This plugin displays a signal meter below the signal data.

Displayed outside or within the SIGNAL container, your choice.

![outside_true](https://github.com/AmateurAudioDude/FM-DX-Webserver-Plugin-S-Meter/assets/168192910/a0b7d7f6-64e7-4664-b94f-d82b0ba90aa6)   
![outside_false](https://github.com/AmateurAudioDude/FM-DX-Webserver-Plugin-S-Meter/assets/168192910/c4085abe-847c-415d-ba09-330563b080a7)

* [Download the latest zip file](https://github.com/AmateurAudioDude/FM-DX-Webserver-Plugin-S-Meter/archive/refs/heads/main.zip)
* Transfer `SignalMeterSmall` folder, and `SignalMeterSmall.js` to FM-DX-Webserver `plugins` folder
* Restart FM-DX-Webserver if required
* Login to Adminstrator Panel and enable plugin

## Options (found at the beginning of `pluginSignalMeterSmall.js`)

`isOutsideField`: Where the S-Meter is to be displayed, within the SIGNAL field, or below it.

`enableSquelch`: Server-side squelch that mutes all signals below the set threshold. Squelch settings does not affect other listeners.

`enableLowSignalInterpolation`: Because approximately -120dBm is the reported noise floor with TEF receivers, the S-Meter will never fall below this level (approx. S4). This attempts to calculate and correct those values based on the signals below -114dBm (just below S6), where true signal deviation from reported signal begins.

`sRepValue` variable calibration: Disconnect antenna and find the quietest noise floor. Adjust value of variable for meter to read just below S1.

v1.2.1
------
* Fix for FM-DX Webserver v1.2.4 compatibility issues

v1.2.0
------
* Added client-side squelch

v1.1.5
------
* Improved alignment based on window dimensions

v1.1.4
------
* Fix for some cases of canvas being cropped

v1.1.3
------
* Corrected decimal place calculations for all signal units

v1.1.2
------
* Aligned signal meter appearance and positioning

v1.1.1
------
* Added option `enableLowSignalInterpolation`
* Signal strength decimal place included in calculations

v1.1
----
* Visual improvements
* Corrected slight signal inaccuracies
* Added lighter grey bar to display signal peak (for current frequency)
* Removed separate image file
* Optional placement within or outside SIGNAL field (edit `pluginSignalMeterSmall.js`)

v1.0
----
* Public release

Original source code located at: https://github.com/NO2CW/FM-DX-Webserver-analog-signal-meter
