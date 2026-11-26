# Karta projektu

Wersja: [1 po P1 / 2 po P2] · Data: [rrrr-mm-dd]

| Pole | Wasza odpowiedź |
| --- | --- |
| Zespół (imiona, loginy GitHub) | |
| Temat (numer z listy albo własny) | |
| Pytanie i odbiorca | |
| Obszar i jednostka analizy | |
| Zmienna celu i źródło etykiet | |
| Dane: źródła, okres, format, licencja, dostęp | |
| Cechy (wstępna lista) | |
| Model bazowy i model AI | |
| Miara sukcesu | |
| Walidacja: jak dzielicie dane i dlaczego | |
| Produkt GIS: warstwa i mapa | |
| Ryzyka i plan B | |

## Szybki test danych (P1)

Wklejcie metryczkę z notatnika `00_start.ipynb`. Mapę `00_start_mapa.png` z folderu `GeoAI_projekt` na Dysku wgrajcie do folderu `wyniki` i wstawcie tu kod `![Mapa z testu danych](../wyniki/00_start_mapa.png)`.

[metryczka]

## Wskazówki

Przykład z W1, bezpieczeństwo pieszych:

- **Pytanie i odbiorca:** które przejścia dla pieszych zmodernizować najpierw; zarządca dróg w mieście.
- **Jednostka:** jedno przejście dla pieszych w Krakowie.
- **Zmienna celu:** liczba wypadków z udziałem pieszych w ciągu 5 lat, SEWIK.
- **Model bazowy i model AI:** liczba wypadków z poprzednich lat; boosting gradientowy.
- **Miara sukcesu:** ile przejść z rzeczywistej pierwszej dwudziestki model stawia w swojej pierwszej dwudziestce.
- **Walidacja:** po dzielnicach i na późniejszym okresie.
- **Ryzyko i plan B:** część zdarzeń bez współrzędnych; plan B: analiza na odcinkach ulic.

Pytanie zaczyna się od decyzji, nie od metody: „które przejścia zmodernizować najpierw”, a nie „zbudujmy sieć neuronową”.
