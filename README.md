![PROJECT_PHOTO](https://raw.githubusercontent.com/alutov/nrf24le1-espnrf_gateway_and_remote_switch_for_livolo_etc/master/other/livolo1.jpg)
![PROJECT_PHOTO](https://raw.githubusercontent.com/alutov/nrf24le1-espnrf_gateway_and_remote_switch_for_livolo_etc/master/other/livolo2.jpg)
![PROJECT_PHOTO](https://raw.githubusercontent.com/alutov/nrf24le1-espnrf_gateway_and_remote_switch_for_livolo_etc/master/other/espnrf3.jpg)
![PROJECT_PHOTO]( https://raw.githubusercontent.com/alutov/nrf24le1-espnrf_gateway_and_remote_switch_for_livolo_etc/master/other/espnrf4.jpg)
# ESP8266+NRF24LE1 MQTT gateway and NRF24LE1 remote switch for livolo etc.

   Gateway code allows to use an ESP8266 and NRF24LE1(espnrf) connected each other via rs232 as a gateway to control NRF24LE1 client by
MQTT server. Connection on gateway side: ESP tx <-> NRF(32pin) p0.4(rx), ESP rx <-> NRF(32pin) p0.3(tx), ESP gpio02 <-> NRF reset. The gateway polls 16 NRF clients, with 4 numeric parameters each. The name of each parameter up to 32 characters must be defined when configuring in the espnrf web interface.
   Client code allows to use NRF24LE1 as a remote two-channel switch with state monitoring and control of both the impulse and the livolo or rcswitch protocol. The first 2 parameters reflect the status of the switches (1/0, on/off, true/false), the third parameter is used to display the temperature from the DS18B20 sensor (relevant for embedding the NRF24LE1 in the air conditioner), the fourth parameter is the supply voltage of the NRF24LE1. Using the assembler without any sdk allowed the client to reduce the clock frequency by 16 times (1MHz), and when generating the RC code MCU works at 125 kHz, and accordingly to reduce power consumption, and in the gateway it is free to store in memory not only the program code, but and reserve space for code updates and for 64 parameter names. More in readme_rus.pdf.



# ESP8266+NRF24LE1 MQTT шлюз и NRF24LE1 беспроводной выключатель для livolo и т.п.

   Gateway код позволяет шлюзу ESP8266 и NRF24LE1(espnrf), соединенными по rs232, управлять NRF24LE1 клиентом  при помощи MQTT сервера.
Соединения на стороне шлюза ESP tx <-> NRF(32pin) p0.4(rx), ESP rx <-> NRF(32pin) p0.3(tx), ESP gpio02 <-> NRF reset. Шлюз опрашивает 16 NRF клиентов, по 4 числовых параметра в каждом. Имя каждого параметра до 32 символов должно быть определено при конфигурации  в espnrf web интерфейсе.  
   Client код позволяет использовать NRF24LE1 как удаленный беспроводной двухканальный выключатель с контролем состояния и управлением как импульсом, так и по протоколу livolo или rcswitch. Первые 2 параметра отражают состояния выключателей (1/0, on/off, true/false), третий параметр используется для вывода температуры с датчика DS18B20 (актуально для встраивания NRF24LE1 в кондиционер), четвертый параметр - напряжение питания NRF24LE1. Использование ассемблера без всяких sdk позволило в клиенте понизить тактовую в частоту в 16 раз(1MHz) , а при генерации RC кода MCU работает на 125 kHz, и соответственно снизить потребление энергии, а в шлюзе свободно вместить в память не только код программы, но и зарезервировать место для обновления кода и для 64 имен параметров. Подробнее в readme_rus.pdf. 
