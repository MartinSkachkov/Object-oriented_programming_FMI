# Семинар 12.05.23

## Задача първа
Да се реализира полиморфна йерархия за работа колекции от цели числа. Всяка от колекциите трябва да съдържа:
* `add`      - Добавя елемент към колекцията.
* `remove`   - Премахва елемент от колекцията.
* `count`    - Връжа колко елемента от този тип имаме.
* `contains` - Връща дали елемента се съдържа в колекцията.

Ща раелизираме следните колекции:
* NormalCollection - Това е стандартната динамична колекция.
  * add      - O(1)
  * remove   - O(n) (remove e O(1) ако премахваме по индекс)
  * count    - O(n)
  * contains - O(n)
* SortedCollection - Колекция в която елементите са сортирани
  * add      - O(n)
  * remove   - O(n)
  * count    - O(log(n))
  * contains - O(log(n)) - двоично търсене.
* IntervalCollection - Колекция, която допуска числа само от определен интервал (примерно [5, 49])
  * add      - O(1)
  * remove   - O(1)
  * count    - O(1)
  * contains - O(1)
* Union - Oбединение на две колекции.
  * add - Добавя елемент и в двете колекции.
  * remove - премахва елемент и от двете колекции
  * count - връща броя в лявата и в дясната колекция
  * contains - връща дали се съдържа в лявата или дясната колекция
* Intersection - Сечение на две колекции.
  * add - добавя в колекцията с по - малко елементи. Когато са равни се добавя и в двете колекции.
  * remove - премахва от колекцията с по - малък брой. Когато са равни се премахва и от двете.
  * count - връща броя в колекцията с по - малко елементи.
  * contains - връща дали елемента се среща и в двете колекции.