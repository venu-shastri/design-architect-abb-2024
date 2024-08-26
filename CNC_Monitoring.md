# CNC Monitoring and Alerting

We need a solution to interpret data coming out of a _CNC-machine monitor_.
Our purpose is to alert when something needs attention.
The alert needs to include information on the area that needs attention -
the machine or the environment.
The personnel that need to be alerted are different in each case.

A basic idea of CNC machines can be seen [here](https://en.wikipedia.org/wiki/Numerical_control).
Keeping these machines safe and reliable is vital in any manufacturing unit.

## Monitored data

The _CNC-machine monitor_ gives the following data:

- Operating temperature: Temperature around the CNC machine in Celsius.
Reported every half-hour. Need to alert if it goes beyond 35 degrees.

- Part-dimension variation: In mm. A variation of more than 0.05 mm needs attention
(example: a drill-bit in the machine may need replacement)

- Duration of continuous operation: Reported in minutes.
Updated once every 15 minutes.
More than 6 hours of continuous operation requires attention.

- Self-test status-code, reported at startup

| Code | Meaning |
|---:|---|
|0xFF|All ok|
|0x00|No data (examples: no power, no connection to the data-collector)|
|0x01|Controller board in the machine is not ok|
|0x02|Configuration data in the machine is corrupted|

Assume that the above data is monitored and passed-on to your program.
You can choose to take the inputs as function calls to your program, or as events.

## Expected outputs

The Solution needs to indicate if there is a need for attention.

When there is a need to attend,
it needs to offer an initial diagnosis,
to help in alerting the appropriate personnel:
It needs to convey whether the machine needs attention,
or if its environment needs attention.


