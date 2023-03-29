# smartcitypriority
A priority-based optimisation service for smart cities, written by Prof. [Daniel G. Costa](https://sigarra.up.pt/feup/pt/FUNC_GERAL.FORMVIEW?p_codigo=514852).

It is a Python3 implementation of temperature sensor nodes (tempsensor) and a central controller (CPM), performing prioritisation for different types of optimisations.

This implementation is a proof-of-concept of the definitions presented in the article A Prioritization Approach for Optimization of Multiple Concurrent Sensing Applications in Smart Cities (https://doi.org/10.1016/j.future.2020.02.067).

The sensor node is executed through the file "tempsensor.py". It requires two additional libraries, which can be installed through the following commands:

```
pip3 install Adafruit_DHT
pip3 install wiringpi
```

Other important remark is when creating the temperature sensor in a Raspberry Pi board. The following variables have to be properly defined in the "tempsensor.py file, according to the implemented connections of the components.

```C
pin1 = LED (yellow);
pin2 = LED (blue);
pin3 = LED (green);
pin4 = LED (red);
pin5 = Button;
pin6 = DHT22 (DATA);
pin7 = TM1637 (CLK);
pin8 = TM1637 (DIO);
```

The CPM is executed through the file "cpm.py".

All configuration tables are defined through a specific txt file in the directoy "tables\". So, there are the "context.txt" for the CT and a subdirectoy "events\", which defines the events priority for each value of a. 
For exemple, for a=1, the file tables\events\1.txt must to be configured.
