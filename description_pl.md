# Problem

## Pytanie

Jak otrzymać jak najbliższy obraz do oryginału za pomocą grafik wektorowych?

## Opis problemu

Mam zbiór 105 grafik wektorowych. Grafiki wektorowe są dostępne w folderze "vector graphics". Spośród 105 grafik wybieramy podzbiór 40 elementowy. Dana grafika może być wybrana kilka razy do podzbioru. Wszystkie operacje od tego momentu są wykonywane na wybranym podzbiorze(40 elementowym).

### Jakie operacje można wykonać na jednej grafice wektorowej?

- Przemieszczanie(z miejsca na miejsce),
- Skalowanie(czyli powiększanie i pomniejszanie),
- Transformacja(czyli z kwadratu można stworzyć prostokąt, deformacja grafiki za pomocą osi x lub y),
- Obracanie(czyli obrót o kilka stopni),
- Odbicie lustrzane(czyli dokonanie odbicia za pomocą osi x lub osi y),

### Scena

Grafiki są umieszczane na scenę o wielkości 966px na 966px. Grafika jest widoczna tylko w obszarze sceny. Jeżeli część grafiki nieznacznie "wychodzi" poza krawędź sceny, to tylko ta część, która znajduje się w obszarze sceny jest widoczna.

### System warstw

Podzbiór wyselekcjonowanych 40 grafik działa w systemie warstw. Można myśleć o tym jak o stosie elementów. Pierwszy element, ktory znajduje sie na samej gorze jest widziany jako pierwszy. Drugi element może zostać(lub nie musi być) zakryty w czesci lub calosci przez element znajdujący się na samej gorze(pierwszy). Taki mechanizm widoczności aplikuje się do wszystkich 40 warstw. Na danej warstwie znajduje się tylko jedna grafika! Oczywiście kolejność grafik/warstw możemy zmieniać. To znaczy grafika na samej górze może zostać grafiką na samym dole. Taki system warstw jest zaimplementowany na przykład w programie Photoshop.

### Kolory

Istnieje wiele technik w jaki sposób można to uzyskać.