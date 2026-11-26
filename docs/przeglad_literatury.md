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

[Ta sama karta.]

## Istniejące rozwiązanie

| Nazwa i link | Kto je prowadzi | Co robi | Czego nie robi, a my zrobimy |
| --- | --- | --- | --- |
| [InPost – znajdź Paczkomat](https://inpost.pl/znajdz-paczkomat) | InPost | Wyświetla istniejące automaty paczkowe i umożliwia ich wyszukiwanie. | Publiczna mapa nie przedstawia rekomendowanych lokalizacji nowych automatów na podstawie modelu GNN. |

## Wnioski dla projektu

Do oceny lokalizacji automatów wykorzystamy dane dotyczące zabudowy, punktów usługowych i sieci drogowej. Zastosujemy GraphSAGE, aby uwzględnić również informacje z sąsiednich komórek H3. Wyniki porównamy z regresją logistyczną, stosując przestrzenny podział danych. Model będzie wskazywał potencjalne lokalizacje nowych automatów na podstawie cech otoczenia, bez przewidywania rzeczywistego popytu na przesyłki.
