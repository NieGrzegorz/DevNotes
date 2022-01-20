# ADC 
The purpose of ADC (Analog-to-digital converter) is to convert conditioned analog signals into a stream of digital data so that a system can process them.   ADC does the counter operation to DAC (Digital-to-analog converter). 
## General 

## ADC in STM32F4
### Terminology 
- Resolution 
- Reference voltage 
- Sampling rate 
- Conversion time 
- Result voltage 
### Features 
- 12-bit resolution 
- Interrupt generation 
- Single and continous conversion modes 
- Scan mode 
- Self-calibration 
- Dual-mode or triple-mode
- Input range : Vref- <= Vin <= Vref+ 

### Channel selection 
There are 16 multiplexed channels. It is possible to organize the convertions in two groups: 
- Regular group -> composed of up to 16 conversions. 
- Injected group -> is composed of up to 4 conversions. 

A group consist of a sequence of conversions that can be done on any channel in any order. 

#### Injected vs regular 
"You can configure the ADC to read in a sequence of channels in a loop. Those channels are being converted regularly. In injected mode conversion is triggered by an external event or by software. An injected conversion has higher priority in comparison to a "regular" conversion and thus interrupts the regular conversions."

source: https://electronics.stackexchange.com/questions/83426/what-is-the-difference-between-an-injected-and-regular-stm32-adc-channel


### Modes
- Single conversion mode 
- Continuous conversion mode 
- Scan mode 
- Discontinuous mode 

### Multi ADC modes 
#### Dual ADC mode 
### ADC Reading methods 

### ADC errors 