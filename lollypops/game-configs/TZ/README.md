###Background
Twilight zone is somewhat unique in the sense that the pop bumpers can have three different states at any one time - off, flashing or on. In order to support these states, we have to wire the Lollypops up slightly differently to normal.

###Connections
J2 (Sensor 1) - Connected to **Lamp 61** (Left Jet Bumper).
J3 (Sensor 2) - Connected to **Lamp 62** (Lower Jet Bumper).
J4 (Sensor 3) - Connected to **Lamp 63** (Right Jet Bumper).
J5 (Sensor 4) - DIP Switch set to 1K (**IMPORTANT**) and connected to **Flasher 17** (Bumpers).

###Configuration
Set the Actions of each LED to below (or import the configuration in this folder).

LED1 At Rest Action = Off
LED1 Trigger Action = Show At Rest Pattern

LED2 At Rest Action = Off
LED2 Trigger Action = Show At Rest Pattern

LED3 At Rest Action = Off
LED3 Trigger Action = Show At Rest Pattern

LED4 At Rest Action = Off
LED4 Trigger Action = Show Random Pattern
LED4 Trigger Target = All LEDs
