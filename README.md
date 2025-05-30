Proyek ini merupakan implementasi sistem terdistribusi berbasis mikrokontroler yang dirancang untuk meningkatkan efisiensi dan keamanan melalui pemantauan lingkungan secara real-time. Dengan mengandalkan sensor-sensor digital dan analog, serta konektivitas internet melalui platform IoT, sistem ini mampu mengirim dan menerima data secara langsung dari perangkat ke pengguna. Tujuan utama dari proyek ini adalah untuk mengintegrasikan berbagai teknologi sensor dengan pengendalian otomatis yang dapat disesuaikan, sambil tetap menjaga fleksibilitas dalam skalabilitas dan penggunaan di berbagai skenario.


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



//f
Fungsi	Widget	Tipe Datastream	Virtual Pin
Temperatur	Gauge / Label	Float	V0
Kelembaban	Gauge / Label	Float	V1
Intensitas Cahaya (LDR)	Gauge / Label	Integer	V2
Kelembaban Tanah (Soil)	Gauge / Label	Integer	V3
Kontrol Relay Manual	Switch	Integer	V4

Opsional: gunakan Notification widget jika ingin memberi notifikasi saat tanah kering.

//h
Fungsi	Widget	Tipe Datastream	Virtual Pin
Temperatur	Gauge / Label	Float	V0
Kelembaban	Gauge / Label	Float	V1
Intensitas Cahaya (LDR)	Gauge / Label	Integer	V2
Buka/Tutup Pintu (Servo)	Switch	Integer	V3
Jarak Orang (Ultrasonic)	Gauge / Label	Float	V4
Status Fingerprint / RFID	Label / Terminal	String	V5 (opsional)

Tambahkan Image Gallery atau Terminal untuk hasil autentikasi RFID/fingerprint (jika digunakan lebih lanjut).

//k
Fungsi	Widget	Tipe Datastream	Virtual Pin
Deteksi Api (Flame)	LED / Label	Integer (0/1)	V0
Kadar Gas (MQ2)	Gauge / Label	Integer	V1
Temperatur Udara (DHT)	Gauge / Label	Float	V2
Status Pompa	LED / Value Display	Integer	V3

Tambahkan Notification untuk memberi peringatan darurat, dan Email jika ingin sistem notifikasi melalui email Blynk.
