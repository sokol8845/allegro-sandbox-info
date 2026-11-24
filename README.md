# Kontrola kont sandbox

Wersja 0.1 · Allegro Sandbox · aplikacja konsolowa do użytku własnego

Aplikacja jest w trakcie konfiguracji. Jej celem jest sprawdzenie, które z własnych kont testowych właściciela udzieliło aplikacji dostępu. Pozwala to przypisać wynik kontroli do właściwego konta.

## Autoryzacja i zakres dostępu

Planowany mechanizm autoryzacji to OAuth 2.0 Device Flow. Właściciel konta testowego otwiera stronę autoryzacji Allegro Sandbox, sprawdza nazwę aplikacji i zatwierdza dostęp dla danego konta.

Jedynym planowanym uprawnieniem jest `allegro:api:profile:read`. Po uzyskaniu tokena użytkownika aplikacja ma wywołać `GET /me` w Allegro REST API Sandbox i porównać zwrócony login z oczekiwanym kontem.

## Ochrona dostępu i danych

Aplikacja jest przeznaczona do uruchamiania na komputerze właściciela. Założeniem konfiguracji jest przechowywanie sekretu klienta i tokenów poza repozytorium oraz pomijanie ich w logach. Do zapisu wyniku kontroli wystarczają alias konta, data i status weryfikacji.

## Kontakt

W sprawach działania i weryfikacji aplikacji: ksoo@intigriti.me
