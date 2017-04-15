# Sensing and Measurements

This list is a compilation of sensor descriptions and some useful calculations.

## Sensors
Sensors come in a few different flavors. Most generally, digital and analog sensors. The majority of sensors RPL uses are analog. Analog sensors have an output that is a continuously variable signal. I.e. it operates in continuous time.

### Load Cells

#### Principle of Operation


#### Practical Concern


### Accelerometers
_**At A Glance**:_ <br>
Accelerometers measures _proper_ acceleration. By incorporating an accelerometer into an inertial measurement system, one can integrate once to obtain a velocity and integrate twice to obtain a position. Many accelerometers are integrated into one chip with a 3-axis accelerometer, 3-axis gyroscope, and 3-axis magnetometer. This 9-axis measurement can be combined with a Kalman filter to obtain accurate data.

#### Principle of Operation


#### Practical Concerns


### Thermocouples
_**At A Glance**:_ <br>
Thermocouples are simple, robust, sensors used to measure temperature. They are inherently analog. Measurements of the voltage can be made to correspond to a temperature given that the material properties of the thermocouples are known. This is known as the _Seebeck Voltage_.

Thermocouples generally have the largest temperature range of sensors. K-type temperature thermocouples have a temperature range of approximately 0 to 1250 C, but it is possible to push the temperature range higher.

#### Overview
Thermocouples consist of two dissimilar materials joined at an electric junction. If both ends are joined, and there is a temperature difference between the joints, a current is generated due to the thermo-electric effect.

If one end is joined (dissimilar metals), and the other is broken, a voltage is generated. This is known as the Seebeck Voltage.

#### Principle of Operation
The thermo-electric effect creates a current in the conductors.

#### Measurements
Requires cold-junction circuit to read temperature.

#### Practical Concerns


## Measurements
### ADC
Analog to Digital Conversion

#### Resolution
The resolution of the ADC limits the
