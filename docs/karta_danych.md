# Karta danych (KM1, koniec P4)

Jedna karta na każdy zbiór, z którego bierzecie etykiety albo ważne cechy. Wzorem są „karty danych”: Gebru T. i in. (2021). Datasheets for Datasets. Communications of the ACM, 64(12), 86–92.

## Overture Maps - Buildings

| Pole | Opis |
| --- | --- |
| Źródło i link | https://docs.overturemaps.org/guides/buildings |
| Licencja i wymagany podpis | ODbL 1.0 |
| Data pobrania | 26.11.2026 |
| Okres i zasięg | Kraków |
| Jednostka obserwacji | Budynek |
| Liczba rekordów (przed i po czyszczeniu) | x |
| Układ współrzędnych | WGS 84 -> EPSG:2180 |
| Zmienna celu i skąd pochodzą etykiety | x |
| Braki i błędy: ile, gdzie, co z nimi zrobiliście | x |
| Kroki przetwarzania (kod: notatnik lub plik w `src`) | x |
| Dane osobowe: czy są, jak je chronicie | Nie są wykorzystywane |

## Atrybuty

| Kolumna | Znaczenie | Jednostka | Braki [%] |
| --- | --- | --- | --- |
| id | Identyfikator budynku| - | x |
| geometry | Geometria budynku | - | x |

## Overture Maps – Places

| Pole | Opis |
| --- | --- |
| Źródło i link | https://docs.overturemaps.org/guides/places |
| Licencja i wymagany podpis | ODbL 1.0 |
| Data pobrania | 26.11.2026 |
| Okres i zasięg | Kraków |
| Jednostka obserwacji | Punkt zainteresowania (POI) |
| Liczba rekordów (przed i po czyszczeniu) | x |
| Układ współrzędnych | WGS 84 -> EPSG:2180 |
| Zmienna celu i skąd pochodzą etykiety | x |
| Braki i błędy | x |
| Kroki przetwarzania | x |
| Dane osobowe | Nie są wykorzystywane |

### Atrybuty

| Kolumna | Znaczenie | Jednostka | Braki [%] |
| --- | --- | --- | --- |
| id | Identyfikator POI | – | x |
| categories | Kategorie obiektu | – | x |
| geometry | Lokalizacja obiektu | – | x |

## Overture Maps – Transportation

| Pole | Opis |
| --- | --- |
| Źródło i link | https://docs.overturemaps.org/guides/transportation/ |
| Licencja i wymagany podpis | ODbL 1.0 |
| Data pobrania |  26.11.2026 |
| Okres i zasięg | Kraków |
| Jednostka obserwacji | Segment sieci transportowej |
| Liczba rekordów (przed i po czyszczeniu) | x |
| Układ współrzędnych | WGS 84 -> EPSG:2180 |
| Zmienna celu i skąd pochodzą etykiety | x |
| Braki i błędy | x |
| Kroki przetwarzania | x |
| Dane osobowe | Nie są wykorzystywane |

### Atrybuty

| Kolumna | Znaczenie | Jednostka | Braki [%] |
| --- | --- | --- | --- |
| id | Identyfikator segmentu | – | x |
| class | Klasa drogi | – | x |
| geometry | Geometria segmentu | – | x |

## OpenStreetMap – Parcel Lockers

| Pole | Opis |
| --- | --- |
| Źródło i link | https://overpass-turbo.eu |
| Licencja i wymagany podpis | ODbL 1.0 |
| Data pobrania | 26.11.2026 |
| Okres i zasięg | Kraków |
| Jednostka obserwacji | Automat paczkowy |
| Liczba rekordów (przed i po czyszczeniu) | x |
| Układ współrzędnych | EPSG:4326 -> EPSG:2180 |
| Zmienna celu i skąd pochodzą etykiety | x |
| Braki i błędy | x |
| Kroki przetwarzania | x |
| Dane osobowe | Nie są wykorzystywane |

### Atrybuty

| Kolumna | Znaczenie | Jednostka | Braki [%] |
| --- | --- | --- | --- |
| id | Identyfikator obiektu | – | x |
| amenity | Typ obiektu | – | x |
| operator | Operator automatu | – | x |
| geometry | Lokalizacja automatu | – | x |

## Zintegrowany zbiór danych

Jednostką obserwacji jest komórka siatki H3.
Wstępnie przyjęto rozdzielczość 9.

### Atrybuty

| Kolumna | Znaczenie | Jednostka | Braki [%] |
| --- | --- | --- | --- |
| h3_id | Identyfikator komórki H3 | – | x |
| building_count | Liczba budynków | szt. | x |
| building_area | Powierzchnia zabudowy | m² | x |
| shop_count | Liczba sklepów | szt. | x |
| poi_count | Liczba wybranych POI | szt. | x |
| road_length | Łączna długość dróg | m | x |
| locker_present | Obecność automatu paczkowego | 0/1 | x |

## Podział na zbiory

- **Schemat:** podział przestrzenny na rozłączne, zwarte obszary w proporcji 60/20/20 w celu ograniczenia
  wpływu autokorelacji przestrzennej.
- **Liczebność:** uczący, walidacyjny, testowy.
- **Mapa zbiorów:** do wygenerowania.
- **Kontrola wycieku:** wykluczenie automatów paczkowych z cech wejściowych, usunięcie krawędzi pomiędzy
  podzbiorami oraz dopasowanie normalizacji wyłącznie na zbiorze uczącym.

## Znane ograniczenia
- Potencjalna niekompletność danych OpenStreetMap.
- Różnice aktualności pomiędzy źródłami danych.
- Brak informacji o rzeczywistym popycie na przesyłki.
- Brak danych o przepustowości i rentowności automatów.
- Brak automatu nie oznacza nieatrakcyjnej lokalizacji.
- Model identyfikuje potencjalne lokalizacje na podstawie
  istniejących wzorców przestrzennych, a nie rzeczywistego
  zapotrzebowania logistycznego.

## Licencje

- [Overture Maps – Attribution](https://docs.overturemaps.org/attribution/)
- [OpenStreetMap – Copyright](https://www.openstreetmap.org/copyright)
