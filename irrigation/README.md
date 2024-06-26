```
Plik: irrigation_esp32_v23.08.4.bin - płytki 8 i 10 przekaźników,
      irrigation_esp32-s3_v23.08.4.bin - 14 przekaźników
```
## `24.05.26`

- **aktualizacja biblioteki**

- **pushover**

  aktualizacja certyfikatu SSL

- **podlewa.cz / crontab**

  zmiana statusu na "odblokowany", kiedy sterownik utracił połączenie z serwerem a nadszedł czas uruchomienia cyklu z wewnętrznego harmonogramu
  
  wydłużenie interwału odpytywania serwera do max. 6 godzin
  
## `23.08.4` (2023-08-15)

- poprawki błędów
- rozszerzenie na wszystkie sekcje w cyklu powiadomienia o braku przepływu

## `23.07.5` (2023-07-13)

- aktualizacja biblioteki SuplaDevice, w tym: _poprawka licznika impulsów, dodanie timer'ów dla przekaźników_
- dodany w ustawieniach wybór ilości powtórzeń cyklu (bazowy czas sekcji jest proporcjonalnie dzielony na ilość powtórzeń)

## `23.05.2` (2023-05-27)

- dodany licznik impulsów (jako opcja w konfiguracji, po włączeniu należy usunąć urządzenie z Cloud, inaczej pojawi się konflikt kanałów)
- rozszerzenie autodozowania na poszczególne sekcje (wcześniej tylko przy cyklu automatycznym)

## `23.04.4` (2023-04-15)

- dodana możliwość ustawienia histerezy auto pazuy

## `23.04.2` (2023-04-03)

- dodany domyślny czas włączenia przekaźnia sekcji - 3 sekundy (kiedy nie jest ustawiony w Cloud czas automatu schodowego)
- usunięty przycisk w GUI - Uruchom/Zakończ ustawienia kanałów

## `23.04.01` (20203-04-02)

- dodany w konfiguracji wybór ilości sekcji podlewania
- dodany w konfiguracji wybór ilości sekcji podlewania w cyklu automatycznym
- dodany w konfiguracji wybór wersji płytki V1 (8 przekaźników) i V2 (10 przekaźników) - jeden plik .bin

Po aktualizacji płytka automatycznie przełączy się do konfiguracji w celu wybrania wersji i ustawienia ilości sekcji.\
W przypadku ustawiania mnijeszej ilości sekcji podlewania (od maksymalnej ilości przekaźników na PCB), pozostałe przekaźniki będzie można dowolnie użyć (np. do włączania oświetlenia)