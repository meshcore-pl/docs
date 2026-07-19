# Terminal Chat CLI

Poniżej znajdują się polecenia, które można wpisywać w klientach Terminal Chat:

```
set freq {frequency}
```
Ustawia częstotliwość LoRa. Przykład: set freq 915.8

```
set tx {tx-power-dbm}
```
Ustawia moc nadawania LoRa w dBm.

```
set name {name}
```
Ustawia nazwę wyświetlaną w advertach.

```
set lat {latitude}
```
Ustawia szerokość geograficzną na mapie w adverta. (stopnie dziesiętne)

```
set lon {longitude}
```
Ustawia długość geograficzną na mapie w adverta. (stopnie dziesiętne)

```
set dutycycle {percent}
```
Ustawia limit cyklu pracy nadajnika (duty cycle, 1-100%). Przykład: `set dutycycle 10` dla 10%.

```
set af {air-time-factor}
```
Ustawia współczynnik czasu nadawania (air-time-factor). Przestarzałe - zamiast tego użyj `set dutycycle`.


```
time {epoch-secs}
```
Ustawia zegar urządzenia przy użyciu sekund epoki UNIX. Przykład: time 1738242833


```
advert
```
Wysyła pakiet advertu

```
clock
```
Wyświetla aktualny czas według zegara urządzenia.


```
ver
```
Pokazuje wersję urządzenia oraz datę kompilacji firmware.

```
card
```
Wyświetla *Twoją* „wizytówkę”, aby inni mogli ją ręcznie _zaimportować_

```
import {card}
```
Importuje podaną wizytówkę do Twoich kontaktów.

```
list {n}
```
Wyświetla listę wszystkich kontaktów od najnowszych. (opcjonalne {n} oznacza ostatnie n według daty advertu)

```
to
```
Pokazuje nazwę aktualnie wybranego kontaktu odbiorcy. (dotyczy kolejnych poleceń „send”)

```
to {name-prefix}
```
Ustawia odbiorcę na _pierwszy_ pasujący kontakt (z „list”) po prefiksie nazwy. (czyli nie musisz wpisywać całej nazwy)

```
send {text}
```
Wysyła wiadomość tekstową (jako DM) do aktualnego odbiorcy.

```
reset path
```
Resetuje ścieżkę do aktualnego odbiorcy, wymuszając ponowne wyszukiwanie ścieżki.

```
public {text}
```
Wysyła wiadomość tekstową na wbudowany, publiczny kanał grupowy „public”.
