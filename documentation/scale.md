# Scale

The scale of the drink mixing machie consists of a beam scale combined with an ADC

## Beam Scale

The beam scale provides us with a continoues analogue signal that has to be converted to a digital signal.

## ADC

The ADC converts the analogue signal from the beam scale to a digital signal, that can be used by the Raspberry PI.
The Drink mixing machine utilizes the HX711 ADC, which is specialiced in converting analogue data from a scale.

### HX711

The HX711 can be used with 10 or 80 samples per second and provides a active low noise programmable gain amplifier (gain = 32, 64, 128).
Each sample consists of a 24 bit value provided in two-complement.

#### Software

The software library in use is copied from [tatobari's hx711py](https://github.com/tatobari/hx711py).

To get correct values from the scale the library requires the user to specify a `REFERENCE_UNIT`.
This value is the factor that scales the received value and has to be determined by experimentation with the setup, as described in [tatobari's example.py](https://github.com/tatobari/hx711py/blob/master/example.py).
