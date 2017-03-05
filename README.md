# ECU Telemetry
Jeti Advanced ECU LUA Script. Easy telemetry displaying, advanced alarms, easy setup, very configurable 

jeti transmitter fw 4.2.2 firmware and vspeak 2.2 firmware required

vspeak lua turbine ecu status converter and alarm script v2 alfa - alfa testers and helpers wanted. PM me.

Supporting:
- Vspeak JetCat (new release this week) (config file format old, needs to be reconfigured, use pbs.jsn as example)
- Vspeak Hornet (config file format old, needs to be reconfigured, use pbs.jsn as example)
- Vspeak Jakadofsky (config file format old, needs to be reconfigured, use pbs.jsn as example)
- Vspeak evoJet / Pahl  (config file format old, needs to be reconfigured, use pbs.jsn as example)
- Vspeak PBS  (config file format OK)
- Orbit (config file format OK)

Supporting a new ecu converter is as easy as adding a json configuration file.

Only tested on DC-24.

Implemented functionality in beta:
- Separate advanced json configuration file for each ECU type (maybe for each turbine type later)
- Possibility to read all statuses by voice
- Possibility to turn on or off alarms globally - if you are annoyed
- Configurable which turbine status enables alarms (to not get false alarms on startup where telemetry is not available). Defaults to alarms enabled when armed status is reached.
- Configurable which switch turns off alarms (recommended same as throttle cut)
- Individually configurable parameters for EVERY turbine STATUS (this is super cool and super flexible)
-- Alarm on status: on or off
-- Audio alarm (information in female voice, warnings in male voice), possibility to change audio file.
-- Haptic feedback, which stick, which vibration profile, on/off
-- Display warning. on/off - shows the status text as a warning.

The usual alarms, but easier setup
- Turbine RPM high
- Turbine RPM low
- Shaft RPM high
- Shaft RPM low
- Ecu voltage high
- Ecu voltage low
- Pump voltage high
- Pump voltage low
- Tank information
- Tank warning
- Tank alarm
- Reading tank level status at configured intervals

Telemetry display
- Turbine status (and only that)
- Reimplemented the telemetry status display code and graphics  from "ECU data display" for Orbit made by Bernd Woköck

Thinking of implementing:
- Warning if you try to shutdown turbine while it is too hot (if possible to implement)
- Later than this: Maybe a cool graphical display of all data like xicoy GSU

Help needed:
- Translation
- Configuration of "best practice" turbine alarms and setup for the supported ecus.
- Generation of audio files for all statuses
- Testing
- Jeti Params for different ECUs (we only have to choose one sensor, we find the rest automatically by param)
- Making videos of running system


So the idea is that with this lua script you will get all needed turbine alarms setup in under 5 minutes (download lua script and install it- chooce ECU type, choose status telemetry sensor - you are done), with our collective best effort on defining whats the best way to have turbine alarms.

For the people who love to tinker it is infinitely extensive and changeable in a easy manner in the configuration file pr ecu. But the distributed configuration file should be best practise for all others.

Installation
- copy ecu.lua and ecu folder into the Apps folder on your Jeti transmitter
- add ecu.lua to applications
- choose ecu type
Then you are up and running


If you have any more ideas about needs for turbine alarms, please let me know.
