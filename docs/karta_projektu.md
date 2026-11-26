# Karta projektu

Wersja: [1 po P1 / 2 po P2] · Data: [rrrr-mm-dd]

| Pole | Wasza odpowiedź |
| --- | --- |
| Zespół (imiona, loginy GitHub) | Mateusz Woźniak mwozniak2180, Jakub Wrzosek j-wrzosek |
| Temat (numer z listy albo własny) | Optymalizacja lokalizacji automatów paczkowych z wykorzystaniem grafowych sieci neuronowych (GNN). |
| Pytanie i odbiorca | Gdzie w Krakowie zlokalizować nowe automaty paczkowe?; Firma zajmująca się dostawami|
| Obszar i jednostka analizy | Kraków |
| Zmienna celu i źródło etykiet | Obecność automatu paczkowego w komórce H3 (0/1); OpenStreetMap (amenity=parcel_locker).|
| Dane: źródła, okres, format, licencja, dostęp | Overture Maps (Buildings, Places, Transportation) – GeoParquet; OpenStreetMap – GeoJSON, ODbL 1.0. Dane aktualne na 26.11.2026r |
| Cechy (wstępna lista) | Liczba budynków, powierzchnia zabudowy, liczba sklepów i punktów usługowych, długość dróg, dostępność komunikacyjna. |
| Model bazowy i model AI | Regresja logistyczna oraz grafowa sieć neuronowa GraphSAGE. |
| Miara sukcesu | Wyższa wartość PR-AUC modelu GNN względem modelu bazowego. |
| Walidacja: jak dzielicie dane i dlaczego | Podział przestrzenny 60/20/20 (trening, walidacja, test), ograniczy to wyciek danych. Uzupełnienie braku danych przed podziałem na zbiory. |
| Produkt GIS: warstwa i mapa | Warstwa GeoPackage w EPSG:2180 zawierająca komórki H3 z oceną potencjału lokalizacyjnego. Mapa rekomendowanych lokalizacji automatów paczkowych.|
| Ryzyka i plan B | Niekompletność danych, niezbalansowane klasy, brak danych o rzeczywistym popycie Plan B: wykorzystanie wyłącznie danych OSM oraz uproszczenie zestawu cech. |

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
