# Задача 2. Сортируем адреса
В этом задании мы будем читать из файла адреса и выводить их в другой файл в другом формате, отсортированными по названию города

Вам дан файл `in.txt`, в котором находится `N` адресов - число `N` идёт первым в файле. После числа `N` располагаются `N` блоков по 4 строки в каждом. Каждый блок состоит из следующих строк: название города, название улицы, номер дома, номер квартиры

Задача программы заключается в том, чтобы считать адреса из файла `in.txt`, отсортировать их по названию города и вывести отсортированный список адресов в файл `out.txt` в другом формате (не забудьте вывести количество адресов в начале)

Города должны быть отсортированы в лексикографическом порядке - то есть в алфавитном

Формат вывода адреса: `<название города>, <название улицы>, <номер дома>, <номер квартиры>`

### Пример работы программы
#### in.txt
```
5
Москва
Строителей
34
12
Новокузнецк
Науки
5
16
Омск
Пушкина
2
13
Москва
Арбат
4
1
Новосибирск
Мира
85
64
```

#### out.txt
```
5
Москва, Строителей, 34, 12
Москва, Арбат, 4, 1
Новокузнецк, Науки, 5, 16
Новосибирск, Мира, 85, 64
Омск, Пушкина, 2, 13
```

#### Подсказки

> Не читайте этот раздел сразу, попытайтесь сначала решить задачу самостоятельно :)

<details>

<summary>Подсказка. Что использовать для решения?</summary>

Для хранения адреса создайте класс (например, `address`). В нём будут поля для хранения названий города и улицы (`std::string`), а также номеров дома и квартиры (`int`)

Создайте в вашем классе конструктор с параметрами, чтобы нельзя было создать пустой адрес

Создайте в вашем классе метод, который собирает строку для вывода в файл (можно назвать его, например, `get_output_address`). Метод будет возвращать значение типа `std::string`

Не забудьте сделать ваши поля приватными - так инкапсуляция вашего класса станет лучше, так как будет меньше потенциальных связей с внешним кодом

Для хранения всех адресов заведите динамический массив типа `address*` - для хранения экземпляров вашего класса

Для считывания адресов используйте цикл `for`

Для сортировки создайте функцию `void sort(address* addresses, int size)`, в которой примените один из известных вам алгоритмов сортировки

Для работы с файлом в режиме чтения используйте класс `std::ifstream`

Для работы с файлом в режиме записи используйте класс `std::ofstream`

</details>