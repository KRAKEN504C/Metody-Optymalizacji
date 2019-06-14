# Dokumentacja Algorytmu levenberga marquardta:
funkcja zawiera algorytm oparty na metodzie marquardta, liczy przybliżone minimum funkcji dwóch zmiennych, i wypisuje to minimum, wraz ze zmiennymi w tym punkcie oraz liczbę iteracji

# Zmienne zewnętrzne:

M - maksymalna ilość kroków algorytmów

epsilon - tolerancja błędu algorytmu.

x - zmienne początkowe

funkcja - funkcja dwóch zmiennych, z której algorytm liczy minimum

# opis:

W metodzie Marquardta, stosuje się na początku metodę Cauchy’ego, a następnie wykorzystuje się metodę Newtona.
Metoda Cauchy’ego jest używana do rozwiązania problemu minimalizacji funkcji.
 
W ogólnym przypadku jest ona wolno zbieżna, więc korzystając z wiedzy o drugiej pochodnej minimalizowanej funkcji w badanym punkcie możemy skorzystać z rozwinięcia gradientu minimalizowanej funkcji w szereg Taylora.
 
Wtedy przyjmujemy przybliżenie kwadratowe funkcji   w otoczeniu   do rozwiązania równania   W ten sposób otrzymujemy metodę Gaussa-Newtona opisaną schematem:
 
 Kenneth Levenberg zauważył, że opisane metody (największego spadku i Gaussa-Newtona) nawzajem się uzupełniają i zaproponował następującą modyfikację kroku metody:
 
Donald Marquardt zauważył, że nawet w sytuacji gdzie hesjan jest niewykorzystywany można wykorzystać informację zawartą w drugiej pochodnej minimalizowanej funkcji, poprzez skalowanie każdego komponentu wektora gradientu w zależności od krzywizny w danym kierunku (co pomaga w źle uwarunkowanych zadaniach minimalizacji typu error valley). Po uwzględnieniu poprawki Marquardta otrzymujemy następującą postać kroku metody:
