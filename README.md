# Program TV

Prosty program telewizyjny w jednym pliku HTML, układ poziomy (oś czasu) jak w odbiorniku TV.
Własna kolejność i widoczność kanałów, dane zapisane w przeglądarce, więc po wczytaniu działa także bez internetu.
Kanały i ich numery pochodzą z listy Telewizji Cyfrowej Play (dawne UPC) dla dekodera Mediabox i modułu CI+ 4K.

**Aplikacja online:** https://romry1966kk.github.io/ProgramTV/

## Jak zacząć

1. Otwórz aplikację w przeglądarce (komputer, iPhone, iPad, Android, Windows, macOS).
2. Wejdź w **Ustawienia → Źródło danych**.
3. Wczytaj dane programu: wpisz adres pliku XMLTV i kliknij **Pobierz teraz**, a jeśli przeglądarka zablokuje pobranie, zapisz plik na dysk (`.xml` lub `.xml.gz`) i wybierz go przyciskiem pod spodem.
4. Pasek u góry pokazuje, na jaki okres są dane i kiedy je wczytano.
5. W części **Kanały** zaznacz kanały, które chcesz widzieć, i ustaw kolejność.

## Obsługa

- **Teraz** przewija tabelę tak, że bieżąca godzina jest na środku. **− / +** zmieniają skalę czasu.
- **Pokaż wszystkie** pokazuje całą listę kanałów, a po odznaczeniu tylko wybrane.
- Kolejność kanałów zmieniasz strzałkami ↑ ↓ i ⤒ (na górę) albo przeciąganiem uchwytu ⠿ lub nazwy kanału w tabeli (przeciąganie działa na komputerze, na dotykowych ekranach używaj strzałek).
- Pod tytułem programu widać dane z pliku: datę, kategorię, kraj, numer odcinka i ocenę, o ile plik je zawiera.
- Jasnoszary blok to program trwający teraz.

## Dane programu

Aplikacja czyta standardowy format **XMLTV**. Przeglądarka nie pozwala stronie pobierać plików z innych serwisów, jeśli serwis sam na to nie zezwala, więc zwykle trzeba:

1. otworzyć adres pliku XMLTV w przeglądarce i zapisać go na dysk,
2. wybrać zapisany plik w Ustawieniach.

Plik wczytuje się raz na kilka dni, zależnie od okresu, który obejmuje program. Po wczytaniu dane są w pamięci przeglądarki. Duży plik (kilkadziesiąt MB) wczytuje się kilkanaście sekund, a postęp jest widoczny w procentach.

Kanały dopasowywane są do pliku automatycznie po nazwie. Znak ⚠ przy kanale w Ustawieniach oznacza brak programu, a ≈ dopasowanie przybliżone. Można wpisać ręcznie identyfikator kanału z pliku w polu „id XMLTV” (podpowiedzi pojawiają się podczas pisania).

## Kopia zapasowa

W Ustawieniach przycisk **Zapisz do pliku** tworzy plik JSON z ustawieniami (kolejność, widoczność, dopasowania) i wczytanym programem. Można go wczytać na innym urządzeniu lub po wyczyszczeniu przeglądarki.

## iPhone i iPad

Safari może usuwać dane stron, z których dawno nie korzystasz. Żeby tego uniknąć, dodaj aplikację do ekranu głównego (przycisk Udostępnij → **Dodaj do ekranu początkowego**) i od czasu do czasu zapisz kopię zapasową.

## Prywatność

Aplikacja nie ma żadnego serwera i niczego nie wysyła. Ustawienia i program są zapisane tylko w Twojej przeglądarce. Połączenie z internetem jest używane wyłącznie wtedy, gdy klikniesz **Pobierz teraz** (albo włączysz automatyczne pobieranie) i tylko pod adres, który sam wpiszesz.

## Rozwój

Cała aplikacja to jeden plik (`index.html`) bez zewnętrznych bibliotek, można go otworzyć lokalnie z dysku lub opublikować np. przez GitHub Pages. Lista kanałów jest wpisana na stałe w skrypcie (stała `RAW`) i pochodzi z dokumentu „Numeracja programów na dekoderze Mediabox i Moduł CI+ 4K” obowiązującego od 12 czerwca 2026 r. Przy zmianie numeracji trzeba ją zaktualizować.

## Uwagi

Dane programu pochodzą z zewnętrznych serwisów XMLTV. Sprawdź warunki ich użycia, zanim udostępnisz kopię pliku publicznie. Nazwy kanałów i programów należą do ich właścicieli.
