# Problem

## Pytanie

W jaki sposób otrzymać jak najbliższy obraz do oryginału za pomocą grafik wektorowych?

## Opis problemu

Mam zbiór 105 grafik wektorowych. Grafiki są dostępne w folderze o nazwie „vector graphics”. Na
potrzeby przedstawienia problemu można założyć, że jest to zbiór symboli lub ikon.

### Jakie operacje można wykonać na jednej grafice?

- Przesunięcie(z miejsca na miejsce oczywiście grafika porusza się i ruch można identyfikować za pomocą
pary [x,y]),
- Skalowanie(powiększanie lub pomniejszanie grafiki bez jej deformacji),
- Transformacja(czyli, modyfikacja grafiki za pomocą długości i szerokości),
- Obracanie(czyli obrót o kilkanaście, kilkaset lub kila stopni),
- Odbicie lustrzane(czyli, zmiana perspektywy grafiki za pomocą długości i szerokości obrazka),

Z głównego zbioru 105 grafik wektorowych możemy wyselekcjonować tylko 40 grafik. W podzbiorze 40
grafik jedna grafika może pojawić się kilka razy. Niekoniecznie musi być to podzbiór unikalnych grafik.

Na podstawie 40 grafik od tego momentu wykonywana jest rekonstrukcja na podstawie oryginalnego
obrazu.

### Scena

Grafiki są umieszczane na scenę o wielkości 966px na 966px. Grafika jest widoczna tylko w obszarze sceny. Jeżeli część grafiki nieznacznie "wychodzi" poza krawędź sceny, to tylko ta część, która znajduje się w obszarze sceny jest widoczna.

### System warstw

Jedna grafika jest równoważna jednej warstwie. To znaczy, że posiadamy 40 warstw. System warstw
możemy rozumieć jako talerz ze stosem naleśników położonych jeden na drugim. Warstwa numer 1 to
warstwa najwyższa. Grafika znajdująca się na tej warstwie jest widoczna jako pierwsza dla obserwatora.
Następnie warstwa nr 2 jest widziana jako druga dla obserwatora. To znaczy, że grafika z warstwy nr 1
może zakryć całkowicie lub nieznacznie grafikę(lub w ogóle nie zakrywać, gdzie pozycja obu grafik się nie
nachodzi) z warstwy nr 2. Ten sposób rozumienia warstw aplikuję się do następnych kolejnych aż do
warstwy nr 40. Taki system warstw jest znany z takich programów jak Photoshop oraz innych służących
do obróbki grafiki wektorowej lub rastrowej.

### Kolory

Kolorowanie i próbkowanie w mojej ocenie jest procesem prostym. Biblioteka open-cv posiada duży
pakiet algorytmów w jaki sposób można to uzyskać.

### Uwagi dodatkowe

Fajnie byłoby jeżeli system w „inteligentny” sposób był w stanie eksperymentować z grafikami. To znaczy
w czasie uczenia się był w stanie wymieniać wszystkie, kilka lub żadnej z grafiki/grafik. Chodzi mi o to,
aby mógł wyznaczyć najbardziej optymalny zbiór 40 grafik, który najbardziej odwzoruję oryginalny obraz.

Z uwagą nr 1 jest powiązany drugi ważny aspekt. To znaczy, fajnie gdyby algorytm był w stanie w
„inteligentny” sposób manipulować kolejnością warstw w taki sposób, aby uzyskać jak najlepsze
odwzorowanie oryginalnej grafiki.