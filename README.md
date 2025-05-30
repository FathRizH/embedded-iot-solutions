//f
🔌 Koneksi Pin:
Komponen	Pin NodeMCU
DHT11/22	D4 (GPIO2)
LDR (via div)	A0
Relay Pompa	D5 (GPIO14)
Soil Sensor	A0 (berbagi input via pemilih)
Buzzer	D6 (GPIO12)
LED indikator	D7 (GPIO13)

Gunakan resistor & multiplexer jika A0 dipakai bersama.

📟 Datastream Blynk (Tipe):
temp (Virtual Pin V0) → Temperature (Float)
humi (V1) → Humidity (Float)
ldr (V2) → Light level (Integer)
soil (V3) → Soil moisture (Integer)
relayControl (V4) → Manual relay (Switch)


//h
🔌 Koneksi Pin:
Komponen	Pin NodeMCU
DHT11/22	D4
LDR	A0
Servo Motor	D5
RFID (RC522)	MOSI/MISO/SCK/SS (D2, D1, D6, D3)
Fingerprint	RX=D7, TX=D8
Ultrasonic	Trig=D1, Echo=D2
Buzzer	D0
LED	D3

📟 Datastream Blynk (Tipe):
temp (V0)
humi (V1)
ldr (V2)
servoControl (V3)
doorStatus (V4)

//k
🔌 Koneksi Pin:
Komponen	Pin NodeMCU
Flame Sensor	D4
DHT11/22	D3
MQ2 Gas	A0
Relay Pompa	D5
Buzzer	D6
LED	D7

📟 Datastream Blynk:
flame (V0)
gas (V1)
temp (V2)
statusPompa (V3)
