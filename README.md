# Saturation meter

A simple saturation meter to estimate the saturation current of inductors.

This project is a quick and dirty implementation, and is not intended for production use. I need to measure the saturation current of some inductors for a project, so I built this tool to help me do that.

I used only parts I had lying around, and I want to use isolation milling, so the design is not optimal.

## Design

It is based on a discussion on the EEVblog forum: https://www.eevblog.com/forum/beginners/help-with-testing-inductor-saturation-current/
The idea is to discharge a capacitor through the inductor and measure the voltage and current across the inductor. When the inductor saturates, the dI/dt increases, (ie L decreases). 

To measure the voltage and current, I use a STM32F103 with its built-in ADC. I choose to not use any op-amps to keep the design simple. 

## ToDo

- [ ] Add more details about the design
- [ ] Add firmware code
- [ ] Add test results