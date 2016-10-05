/*
 MODULE 1 of JEROEN'S DOMOTICA-PROJECT
/*  The code below is my first ESP-project and based on the AdvancedWebserver lib.. I've tried to combine as many I/O facilities 
 *   as I might need, just to get an idea of the capabilities of the chip... The big advantage of this code is that there is a feedback on the outputs!!!
 *   So after your command you can check if the pin is aqctualy high or low!
 *   Not being a professional programmer, but an electronics engineer (1972....) I like it!
 *   What things nowedays can do...
 *   
 *   The code includes temperature, humidity, pressure, lux, sensing and a four chanel ADC (ADS1115) and a small LCD device for local outputs.
 *   It is a very simpel and stabel way of sensing and acuating through a local web page using your local network.
 *   
 *   By playing around one discovers... I'm still playing so the code is not formaly perfect and lean but it works in a stabel way!
 *   
 *   Html page 192.168.2.50 displays the values and 192.168.2.50/socket1On displays the commands
 *   
 *   There is a software ESP-RESTART function implemented. Activation is possible on command (via the web) but that implies a connection of course
 *   and is only sensible if a restart would correct an initialisation problem (f.i. sensors) or resetting variables...
 *   and from a software error (not implemented yet) and from a hardware (interrupt?) situation.
 *   These two options are not yet implemented not yet implemented.
 *   
 *   In the code below I used digitalWrite in the loop-code, 
 *   but analogWrite can be used as well if there is an need for PWM

 *   f.i.
 *   ADC=analogRead(A0);
 *   analogWrite(gpio5_pin,ADC);
 *   PWM1=ADC; 
 *   
 *   *   The pins for I2C can be defined by f.i. Wire.begin(12,13) where 12=SDA, 13=SCL
 
