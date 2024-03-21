# Problem

## Pytanie

Jak otrzymac jak najblizszy obraz do oryginalu za pomoca grafik wektorowych?

## Opis problemu

Mam zbior 105 grafik wektorowych. Grafiki wektorowe sa dostepne w folderze "vector graphics". Z sposrd 105 grafik wybieramy podzbior 40 elementowy. Dana grafika moze byc wybrana kilka razy do podziobru. Wszystkie operacje od tego momentu sa wykonywane na wybranym podzbiorze(40 elementowym).

### Jakie operacje mozna wykonac na jednej grafice wektorowej?

- Przemieszczanie(z miejsca na miejsce),
- Skalowanie(czyli powiekszanie i pomniejszanie),
- Transformacja(czyli z kwadratu stworzyc prostokat, deformacja grafiki za pomoca osi x lub y),
- Obracanie(czyli obrot o kilka stopni),
- Odbicie lustrzane(czyli dokonanie odbicia za pomoca osi x lub osi y),

### Scena

Grafiki sa umieszczane na scene o wielkosci 966px na 966px. Grafika jest widoczna tylko w obszarze sceny. Jezeli czesc grafiki nieznacznie "wychodzi" poza krawedz sceny, to tylko ta czesc, ktora znajduje sie w obszarze sceny jest widoczna.

### System warstw

Podzbior wyselekcjonowanych 40 grafik dzila w systemie warstw. Mozna myslec o tym jak o stosie elementow. Pierwszy element, ktory znajduje sie na samej gorze jest widziany jako pierwszy. Drugi element moze zostac(lub nie musi byc) zakryty w czesci lub calosci przez element znajdujacy sie na samej gorze(pierwszy). Na danej wartwie znajduje sie tylko jedna grafika! Oczywiscie kolejnosc grafik/warstw mozemy zmieniac. To znaczy grafika na samej gorze moze zostac grafika na samym dole. Taki system wartstw jest zaimplementowany na przyklad w programie Photoshop.

### Kolory

Oczwiscie, jezeli chcemy odwzorowac oryginalny obraz. Nalezy probkowac i kolorowac wybrane grafiki. Istnieje wiele technik w jaki sposob mozna to uzyskac.