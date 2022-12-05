
======MQTTBOX (Server-Client MQTT Protocol)======
  MQTT Client
	Host		= test.mosquitto.org
	Port		= 1883
	Client Name 	= porogapit-master
  
  MQTT Topics
    Slave 1 (Wemos D1 Mini Pro)
	temperature		= porogapit/temp1
	pressure 		= porogapit/pres1
	altitude 		= porogapit/alti1
	rssi 			= porogapit/rssi1
	slave1 			= porogapit/snr1

   Slave 2 (ESP32 v1)
	temperature		= porogapit/temp2
	humidity		= porogapit/humi2
	soil moisture		= porogapit/soil_mois2
	soil temperature	= porogapit/soil_temp2
	soil ec			= porogapit/soil_ec2
	soil ph			= porogapit/soil_ph2
	rssi			= porogapit/rssi2
	snr			= porogapit/snr2

======NodeRed (DASHBOARD)======
  Slave 1 (Wemos D1 Mini Pro)
    -BMP280
	Chart 1 -> Ambient Temperature
	Chart 2 -> Ambient Pressure
	Chart 3 -> Ambient Altitude
    -LoRa 
	Chart 4 -> RSSI
	Chart 5 -> SNR 	

  Slave 2 (ESP32 v1)	
    -AHT10
	Chart 1 -> Ambient Humidity
	Chart 2 -> Ambient Temperature
    -NPK Sensor [5 Probe, 5 Parameters]
	Chart 3 -> Soil Temperature
	Chart 4 -> Soil Humidity
	Chart 5 -> Soil EC
	Chart 6 -> Soil pH
    -LoRa 
	Chart 7 -> RSSI
	Chart 8 -> SNR 
