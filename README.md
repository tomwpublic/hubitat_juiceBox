# hubitat_juiceBox

This provides various driver capabilities for Hubitat with JuiceBox EVSE systems.  For each JuiceBox unit, these values are reported during an active charging session: voltage, power, energy, charging status.

Note that all operations have a cloud (internet) interaction.  This implementation is based on the work shared here:  https://github.com/jesserockz/python-juicenet

# Manual Installation instructions:

* In the *Drivers Code* section of Hubitat, add the juiceNetSystem and juiceNetUnit drivers.
* In the *Devices* section of Hubitat, add a *New Virtual Device* of type JuiceNet System
* On the configuration page for the newly created *Device*, enter your JuiceNet API token from your JuiceNet dashboard and *Save Preferences*.
* Use the *createChildDevices* command to generate a child JuiceNet Unit device for each configured charging unit in your system.

# Usage instructions:

* Use built-in dashboard templates for the various measurements.
* Use either *on()* or the custom command *setOverride()* interchangeably to begin charging immediately regardless of schedule.
* Use either *off()* or the custom command *clearOverride()* interchangeably to stop charging and revert to the normal schedule.

# Disclaimer

I have no affiliation with any of the companies mentioned in this readme or in the code.  I also don't have a JuiceBox charger, so my ability to troubleshoot will be limited.
