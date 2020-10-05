Sonoff MINI, BASIC R2, DUAL, 2CH, 4CH R2 - `sonoff_8285_v1.6.bin`  
Sonoff S20, S26 - `sonoff_8266_v1.6.bin`  

Moduł uruchomi się w trybie konfiguracji, rozgłaszając swoją sieć `ESP_XXXXXX`, hasło: `configpass`.

Po połączeniu z siecią wchodzimy w przeglądarce na adres: **192.168.4.1**. Wypełniamy wszystkie pola
```
Username, Password - dowolne
SSID, WPA - dane naszej sieci WiFi
Server, Email - dane SUPLI
```
wybieramy wersję urządzenia i klikamy SAVE to EEPROM - moduł uruchomi się w trybie OTA (jeśli ESP nie podłączy się do naszej sieci, przejdzie ponownie w tryb konfiguracji).

Wchodzimy w przeglądarce na adres, tym razem przydzielony przez router (dane logowania z konfiguracji) i klikamy SWITCH TO SUPLA, 

Po odświeżeniu strony, dla każdego przekaźnika ustawiamy typ: RELAY albo LIGHT RELAY
```
LightRelay to przekaźnik dedykowany do oświetlenia z opcją programowania czasu żywotności źródła światła.  
Taki kanał po kliknięciu w aplikacji na ikonkę (i) pozwala zobaczyć dodatkowe informacje związane z żywotnością  
źródła światła oraz łącznym czasem włączenia.  
Z aplikacji można ustawić żywotność oraz resetować licznik.
```

opcjonalnie ustawiamy nazwę, ilość wirtualnych przekaźników i domyślny stan po utracie i przywruceniu zasilania. Zapisujemy, klikając SAVE and REBOOT.

**`Każda zmiana typu przekaźnika wymaga usunięcia urządzenia z Cloud`**

Miganie diody (ms):
- 100/150 - tryb konfiguracji,
- 1200/150 - tryb OTA,
- 150/1200 - tryb SUPLA, brak połączenia z serwerem,
- 250/250 - brak połączenia z siecią w trybie OTA i SUPLA,
- ciągłe świecenie - tryb SUPLA, połączony z serwerem (możliwe wyłączenie)

Przejście do konfiguracji (config button - tylko w trybie SUPLA):
- monostabilny: wciskamy, przytrzymujemy min. 7s (dioda zacznie migać jak w trybie konfiguracji), puszczamy
- bistabilny: w czasie 7s przełączamy 7 razy (początkowa pozycja nie jest istotna)

---
- crystalFreq 26M
- spiSpeed 40MHz
- spiMode DOUT 0x0
- baudRate 115200
- flashSize 8Mbit (1MByte)
