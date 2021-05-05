Moduł uruchomi się w trybie konfiguracji, rozgłaszając swoją sieć `ESP-XXXXXX`.

Po połączeniu z siecią wchodzimy w przeglądarce na adres: **192.168.4.1**. Wypełniamy wszystkie pola
```
nazwa użytkownika, hasło użytkownika - dowolne
nazwa sieci WiFi, hasło - dane naszej sieci WiFi
serwer Sulpi, adres email - dane SUPLI
```
i klikamy ZAPISZ I URUCHOM PONOWNIE - moduł uruchomi się w trybie OTA (jeśli ESP nie podłączy się do naszej sieci, przejdzie ponownie w tryb konfiguracji). Po odświeżeniu strony pojawi się okno logowania (dane z konfiguracji). Zapisujemy adres IP przydzielony urządzeniu z naszej sieci lokalnej i klikamy PRZEŁĄCZ DO SUPLI.  
(Urządzenie na chwilę przestaje udostępniac sieć podczas ponownego uruchomienia. Jeśli strona nie załaduje się poprawnie, ponownie łączymy się z udostępnianą siecią).

W następnym kroku wchodzimy w przeglądarce na adres z naszej sieci lokalnej (zapisany wcześniej), ponownie podajemy dane logowania. Opcjonalnie ustawiamy nazwę urządzenia i reakcję przycisków. Zapisujemy, klikając ZAPISZ I URUCHOM PONOWNIE.

Miganie diody (ms):
- 100/150 - tryb konfiguracji,
- 1200/150 - tryb OTA,
- 150/1200 - tryb SUPLA, brak połączenia z serwerem,
- 250/250 - brak połączenia z siecią w trybie OTA i SUPLA,
- ciągłe świecenie - tryb SUPLA, status "Zarejestrowany i gotowy" (możliwe wyłączenie)

Przejście do konfiguracji (tylko w trybie SUPLA):
- klikamy 5 razy przyciskiem w górę (ilość kliknięć można zmienić)

---
- crystalFreq 26M
- spiSpeed 40MHz
- spiMode DOUT 0x0
- baudRate 115200
- flashSize 8Mbit (1MByte)
