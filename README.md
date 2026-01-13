# Proiect_ESP
Proiectul constă în proiectarea și construcția unui robot mobil (rover) capabil să fie controlat de la distanță mare prin intermediul unui protocol radio personalizat, utilizând module ESP32 și antene externe.


#BOM (Bill Of Materials) 


| Componentă | Cantitate | Descriere / Rol în Proiect |
|---|---:|---|
| ESP32 DevKit V1 (Model 38 pini) | 2 | Unitățile centrale: una pentru telecomandă (Transmițător) și una pentru robot (Receptor). |
| Antenă Externă 2.4GHz (SMA) | 2 | Crește raza de acțiune și oferă proiectului un aspect tehnic complex. |
| Cablu Pigtail IPEX la SMA | 2 | Face legătura între conectorul mic de pe placa ESP32 și antena externă. |
| Driver de Motor L298N | 1 | Permite controlul puterii și direcției motoarelor de curent continuu. |
| Șasiu Robot (2WD sau 4WD) | 1 | Structura fizică a robotului, include motoarele și roțile. |
| Senzor Ultrasonic HC-SR04 | 1 | Folosit pentru „inteligența” robotului (evitarea automată a coliziunilor). |
| Acumulatori Li-ion 18650 (3.7V) | 2 | Sursa de alimentare principală pentru motoare și electronica robotului. |
| Modul Joystick sau Potențiometre | 1 | Interfața de control pentru utilizator (montată pe telecomandă). |
| Breadboard & Fire Jumper | 1 set | Pentru realizarea conexiunilor electrice fără lipire (în faza de prototip). |
| Regulator de tensiune (opțional) | 1 | Pentru a asigura un curent stabil de 5V către plăcile ESP32. |
