# Przegląd literatury i istniejących rozwiązań

Co najmniej 2–3 artykuły na zespół, w tym jeden recenzowany; każda osoba opisuje co najmniej jeden. Jedna karta na artykuł, jak na seminarium S1: przy każdym pytaniu odpowiedź z artykułu i ocena: tak, częściowo albo nie.

# Przegląd literatury i istniejących rozwiązań

## Artykuł 1

- **Opis bibliograficzny:** Hamilton W. L., Ying R., Leskovec J. (2017). Inductive Representation Learning on Large Graphs. Advances in Neural Information Processing Systems, 30.
- **Link:** https://arxiv.org/abs/1706.02216
- **DOI (preprint):** 10.48550/arXiv.1706.02216
- **Opisuje:** Mateusz Woźniak

| Pytanie | Odpowiedź z artykułu | Ocena |
| --- | --- | --- |
| 1. Problem | Klasyfikacja wierzchołków grafu, również takich, których model nie widział podczas treningu. Brak określonego horyzontu czasowego. | Tak |
| 2. Dane | Grafy publikacji naukowych, postów Reddit oraz interakcji między białkami. Nie ustalono procentowego udziału braków danych. | Częściowo |
| 3. Podział | Model sprawdzono na nowych wierzchołkach oraz grafach niewykorzystywanych podczas treningu. | Tak |
| 4. Punkt odniesienia | Porównano GraphSAGE z innymi metodami, m.in. DeepWalk oraz klasyfikacją wykorzystującą same cechy wierzchołków. | Tak |
| 5. Metryki | Micro-F1 dla poszczególnych zbiorów danych. | Tak |
| 6. Ablacja | Porównano różne sposoby agregowania informacji od sąsiednich wierzchołków. | Tak |
| 7. Powtarzalność | Udostępniono kod i dane eksperymentalne. | Tak |
| 8. Ograniczenia | Skuteczność zależy od jakości cech wierzchołków oraz struktury grafu. | Częściowo |

**Co bierzemy do projektu:** Architekturę GraphSAGE, która pozwala uwzględnić cechy sąsiednich komórek H3 i zastosować model w innych miastach.


## Artykuł 2

## Artykuł 2

- **Opis bibliograficzny:** Elomiya A., Křupka J., Simic V., Švadlenka L., Jovčić S., Pamucar D. (2026). A GIS-MCDM framework for the smart parcel locker site suitability analysis and optimizing urban last-mile delivery. Applied Soft Computing, 198, 115247.
- **Link:** https://doi.org/10.1016/j.asoc.2026.115247
- **DOI:** 10.1016/j.asoc.2026.115247
- **Opisuje:** Jakub Wrzosek

| Pytanie | Odpowiedź z artykułu | Ocena |
| --- | --- | --- |
| 1. Problem | Wyznaczenie odpowiednich lokalizacji nowych automatów paczkowych w Pardubicach w Czechach. | Tak |
| 2. Dane | Dane przestrzenne dotyczące infrastruktury, dostępności komunikacyjnej i zaludnienia. Nie ustalono okresu i procentu braków danych. | Częściowo |
| 3. Podział | Analizę przeprowadzono dla jednego miasta. Metoda nie wymaga klasycznego podziału na zbiór treningowy i testowy. | Nie |
| 4. Punkt odniesienia | Zastosowano analizę wielokryterialną zamiast klasycznego modelu uczenia maszynowego. | Nie |
| 5. Metryki | Ocena przydatności lokalizacji oraz ranking 50 potencjalnych miejsc metodą TOPSIS. | Częściowo |
| 6. Ablacja | Przeprowadzono analizę wrażliwości, sprawdzając wpływ zmiany wag poszczególnych kryteriów na wyniki. | Częściowo |
| 7. Powtarzalność | Opisano metodykę, a dane udostępniono w repozytorium Zenodo. | Częściowo |
| 8. Ograniczenia | Wyniki zależą od przyjętych kryteriów i ich wag. Nie potwierdzono skuteczności na innych miastach. | Częściowo |

**Co bierzemy do projektu:** Wykorzystanie dostępności komunikacyjnej, infrastruktury oraz cech otoczenia do oceny potencjalnych lokalizacji automatów paczkowych.

## Istniejące rozwiązanie

| Nazwa i link | Kto je prowadzi | Co robi | Czego nie robi, a my zrobimy |
| --- | --- | --- | --- |
| [InPost – znajdź Paczkomat](https://inpost.pl/znajdz-paczkomat) | InPost | Wyświetla istniejące automaty paczkowe i umożliwia ich wyszukiwanie. | Publiczna mapa nie przedstawia rekomendowanych lokalizacji nowych automatów na podstawie modelu GNN. |

## Wnioski dla projektu

Do oceny lokalizacji automatów wykorzystamy dane dotyczące zabudowy, punktów usługowych i sieci drogowej. Zastosujemy GraphSAGE, aby uwzględnić również informacje z sąsiednich komórek H3. Wyniki porównamy z regresją logistyczną, stosując przestrzenny podział danych. Model będzie wskazywał potencjalne lokalizacje nowych automatów na podstawie cech otoczenia, bez przewidywania rzeczywistego popytu na przesyłki.
