# Badania Internetowe 2024/25

## Sylabus i materiały

0.  [pakiety `sampling`, `survey` w R i `samplics` w Python](https://htmlpreview.github.io/?https://github.com/DepartmentOfStatisticsPUE/bi-2025/blob/main/notebooks/00-survey.html))
1.  Internet w Polsce
2.  Google Trends
3.  Web-scraping i API
4.  Dobór próby w badaniach internetowych
5.  Reprezentatywność
6.  Metody quasi-randomizacyjne
    - [Porównywanie rozkładów](https://htmlpreview.github.io/?https://github.com/DepartmentOfStatisticsPUE/bi-2025/blob/main/notebooks/05-porownywanie-rozkladow.html)
    - [Wstęp do IPW](https://htmlpreview.github.io/?https://github.com/DepartmentOfStatisticsPUE/bi-2025/blob/main/notebooks/06-ipw-1.html)
    - [Kalibrowany estymator IPW](https://htmlpreview.github.io/?https://github.com/DepartmentOfStatisticsPUE/bi-2025/blob/main/notebooks/06-ipw-2.html)
7.  Model oparte na modelu
8.  Metody podwójnie odporne
9.  Inne metody estymacji

## Projekt

-   [Szablon projektu](zaliczenie/szablon.qmd)
-   [Przykład raportu](https://htmlpreview.github.io/?https://github.com/DepartmentOfStatisticsPUE/bi-2025/blob/main/zaliczenie/projekt-przyklad.html)

## Opis zbioru danych

Dane zawierają następujące kolumny

-   id_popyt -- czy rekord pochodzi z badania ''Popyt na pracę''
-   id_jednostki -- identyfikator jednostki (hash)
-   waga -- waga finalna (badanie ''Popyt na Pracę'', $w$)
-   sek -- sektor (1= publiczny, 2 = prywatny )
-   klasa_pr -- klasa wielkości podmiotu (M=Małe, S=Średnie, D=Duże)
-   woj -- województwo (02,04,...,32)
-   zawod_kod2 -- 2 cyfrowy kod zawodu
-   wolne_miejsca -- liczba wolnych miejsc pracy zgłoszonych w badaniu
    Popyt na pracę
-   id_cbop -- czy rekord pochodzi z CBOP
-   jedna_zmiana -- czy rekord dot. wakatów oferowanych na jedną zmianę
-   wymiar_40 -- czy rekord dot. wakatów w wymiarze 40 godzin
-   wolne_miejsca_cbop -- liczba wolnych miejsc pracy z CBOP
-   wolne_miejsca_niepeln_cbop -- liczba wolnych miejsc pracy z CBOP dla
    osób niepełnosprawnych

Dane wyglądają następująco:

``` r
       id_popyt                             id_jednostki waga sek klasa_pr sekc_pkd woj zawod_kod2 wolne_miejsca id_cbop jedna_zmiana wymiar_40 wolne_miejsca_cbop wolne_miejsca_niepeln_cbop
    1:        1 a9cc990df6a99ab215a1bc13f51d4825c7d52d18    1   1        D        O  14          1             2      NA           NA        NA                 NA                         NA
    2:        2 a9cc990df6a99ab215a1bc13f51d4825c7d52d18    1   1        D        O  14          2             7      NA           NA        NA                 NA                         NA
    3:        3 c9dbaf50890165ebe810aa770de0e9df903dc35b    6   1        D        O  24          2             6      NA           NA        NA                 NA                         NA
    4:        4 718e0bba42bcec6ed98f9690db6d26cb7b93c880    1   1        D      R.S  14          2             7      NA           NA        NA                 NA                         NA
    5:        5 532a1879a692b9d7bbb7282ba757d028156ef341    1   1        D      R.S  14          2             6      NA           NA        NA                 NA                         NA
   ---                                                                                                                                                                                       
20942:       NA a6a20c0f40c36af79446a53cb1af98dac84ca2cf   NA   2        S        G  08          9            NA       1         TRUE      TRUE                  2                          1
20943:       NA 5ab1d632da4eda181d7a454f71dd69e4433b6aa5   NA   2        D        H  08          9            NA       1        FALSE      TRUE                  1                          0
20944:       NA a108d5030e205dc1632b5b8b3eddb725821adfa5   NA   2        S        I  08          7            NA       1         TRUE      TRUE                  1                          0
20945:       NA a108d5030e205dc1632b5b8b3eddb725821adfa5   NA   2        S        I  08          9            NA       1         TRUE      TRUE                 15                          0
20946:       NA d5c8a81acfb94539956a0d87c37a233e21ec435f   NA   2        M        H  08          7            NA       1        FALSE      TRUE                  1                          0
```
