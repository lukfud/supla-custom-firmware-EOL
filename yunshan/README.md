Moduł uruchomi się w trybie konfiguracji, rozgłaszając swoją sieć `ESP-XXXXXX`

Po połączeniu z siecią wchodzimy w przeglądarce na adres: **192.168.4.1**. Wypełniamy wszystkie pola
```
nazwa użytkownika, hasło użytkownika - dowolne
nazwa sieci WiFi, hasło - dane naszej sieci WiFi
serwer Sulpi, adres email - dane SUPLI
```
opcjonalnie kontrolę LED
```
Ustawiając kontrolę LED na TAK będzie można włączać/wyłączać diodę statusu z app/Cloud  
poprzez dodatkowy wirtualny przekaźnik.
```

i klikamy ZAPISZ I URUCHOM PONOWNIE - moduł uruchomi się w trybie OTA - jeśli ESP nie podłączy się do naszej sieci, przejdzie ponownie w tryb konfiguracji, jeśli się  połączy przejdzie automatycznie do trybu SUPLA).

W następnym kroku wchodzimy w przeglądarce na adres z naszej sieci lokalnej, podajemy dane logowania i opcjonalnie ustawiamy nazwę urządzenia. Zapisujemy, klikając ZAPISZ I URUCHOM PONOWNIE.

**`Każde włączenie/wyłączenie kontroli LED wymaga usunięcia urządzenia z Cloud`**

Miganie diody (ms):
- 100/150 - tryb konfiguracji,
- 1200/150 - tryb OTA,
- 150/1200 - tryb SUPLA, brak połączenia z serwerem,
- 250/250 - brak połączenia z siecią w trybie OTA i SUPLA,
- ciągłe świecenie - tryb SUPLA, status "Zarejestrowany i gotowy" (możliwe wyłączenie)

Przejście do konfiguracji (tylko w trybie SUPLA):
zwieramy pin0 z masą, przytrzymujemy min. 5s (dioda zacznie migać jak w trybie konfiguracji), puszczamy - czas można zmienić.


---
- crystalFreq 26M
- spiSpeed 40MHz
- spiMode DOUT 0x0
- baudRate 115200
- flashSize 32Mbit (4MByte)
