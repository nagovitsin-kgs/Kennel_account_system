# Итоговая контрольная работа

## Информация о проекте

Необходимо организовать систему учета для питомника в котором живут домашние и Pack animals.

## Как сдавать проект

Для сдачи проекта необходимо создать отдельный общедоступный репозиторий(Github, gitlub, или Bitbucket). Разработку вести в этом репозитории, использовать пул реквесты на изменения. Программа должна запускаться и работать, ошибок при выполнении программы быть не должно. Программа, может использоваться в различных системах, поэтому необходимо разработать класс в виде конструктора.

## Задание

## Операционные системы и виртуализация (Linux)

1. Использование команды cat в Linux

    - Создать два текстовых файла: "Pets"(Домашние животные) и "Pack animals"(вьючные животные), используя команду `cat` в терминале Linux.
      В первом файле перечислить собак, кошек и хомяков.
      Во втором — лошадей, верблюдов и ослов.
    - Объединить содержимое этих двух файлов в один и просмотреть его содержимое.
    - Переименовать получившийся файл в "Human Friends"(.
    - Пример конечного вывода после команды “ls”:

        Desktop Documents Downloads HumanFriends.txt Music PackAnimals.txt Pets.txt Pictures Videos

Команда cat в Linux используется для чтения, создания и объединения файлов. Она позволяет
просматривать содержимое файлов, а также выводить их на экран или записывать в другие
файлы.
Для решения поставленной задачи нам потребуется выполнить несколько шагов:

1. Создание двух текстовых файлов "Pets" и "Pack animals". Для этого используем команду `cat`
   с символом `>` для перенаправления вывода в файл. В терминале Linux выполняем
   следующие команды:

```
cat > Pets.txt
```

После выполнения данной команды терминал переводится в режим ввода. Перечислим в
нем домашних животных (собак, кошек и хомяков), каждый на новой строке. После ввода
всех животных нажимаем `Ctrl + D`, чтобы завершить режим ввода и создать файл.
Аналогичным образом создаем файл "PackAnimals.txt":

```
cat > PackAnimals.txt
```

Вводим в него список вьючных животных (лошадей, верблюдов и ослов), каждый на новой
строке. Завершаем режим ввода, нажимая `Ctrl + D`.

2. Объединение содержимого двух файлов в один. Для этого используем команду `cat` с
   символом `>>` для добавления содержимого в файл. Выполняем следующую команду:

```
cat Pets.txt >> PackAnimals.txt
```

Эта команда добавит содержимое файла "Pets.txt" в конец файла "PackAnimals.txt". Теперь
файл "PackAnimals.txt" содержит все животных из обоих файлов.

3. Просмотр содержимого объединенного файла. Для этого снова используем команду `cat`:

```
cat PackAnimals.txt
```

Эта команда выведет на экран содержимое файла "PackAnimals.txt", в котором содержатся все
животные.

4. Переименование файла "PackAnimals.txt" в "HumanFriends.txt". Для этого используем
   команду `mv` (от англ. "move") с указанием старого имени файла и нового имени:

```
mv PackAnimals.txt HumanFriends.txt
```

Теперь файл "PackAnimals.txt" называется "HumanFriends.txt".
После выполнения всех этих шагов, при выполнении команды `ls` выведется список файлов и
папок в текущей директории:

```
HumanFriends.txt  Pets.txt
```

Здесь "HumanFriends.txt" и "Pets.txt" - это созданные нами текстовые файлы, а остальные
элементы списка - это другие файлы и папки в текущей директории.

![Task 1](/Task1.png)

2. Работа с директориями в Linux
    - Создать новую директорию и переместить туда файл "Human Friends".

![Task 2](/Task2.png)

3. Работа с MySQL в Linux.

    - Установить MySQL на вашу вычислительную машину.
    - Подключить дополнительный репозиторий MySQL и установить один из пакетов из этого репозитория.

![Task 3](/Task3.png)

4. Управление deb-пакетами.
    - Установить и затем удалить deb-пакет, используя команду `dpkg`.

Установка и удаление deb-пакетов является одной из основных задач в Linux. Для этого
существует утилита dpkg. В данном ответе будет рассмотрено, как установить и удалить debпакеты с помощью dpkg.
Deb-пакеты являются основным форматом пакетов в Debian и его производных
дистрибутивах, таких как Ubuntu. Они содержат программные компоненты, такие как
исполняемые файлы, скрипты установки и другие файлы, необходимые для установки
программного обеспечения.
Прежде чем начать, необходимо убедиться, что у вас есть права суперпользователя или вы
можете выполнить команды с использованием sudo.
Установка deb-пакета с помощью dpkg выполняется следующей командой:

```
sudo dpkg -i имя_файла.deb
```

Где имя_файла.deb - это имя файла deb-пакета, который вы хотите установить.
После выполнения этой команды dpkg начнет процесс установки пакета. Он распакует файлы
в указанное место и выполнит необходимые действия, такие как обновление информации о
пакетах в системе.
Возможно, у вас могут возникнуть ошибки в процессе установки пакета. Они связаны с
зависимостями пакетов. Некоторые пакеты требуют наличия других пакетов для работы, и
если эти зависимости не будут выполнены, установка не будет успешной.
Чтобы устранить проблемы с зависимостями, можно использовать команду apt, чтобы
автоматически установить эти зависимости:

```
sudo apt -f install
```

Эта команда попытается установить все недостающие зависимости и зависимости,
несовместимые с уже установленными пакетами.
Чтобы удалить установленный deb-пакет, используйте команду:

```
sudo dpkg -r имя_пакета
```

Где имя_пакета - это имя установленного пакета, который вы хотите удалить.
Также можно использовать команду dpkg --purge для удаления deb-пакета вместе с его
конфигурационными файлами:

```
sudo dpkg --purge имя_пакета
```

Эта команда удалит все файлы, связанные с пакетом, и удалит его из системы.
Если у вас есть deb-пакет, необходимо установить, или вы хотите удалить пакет, уже
установленный на вашей системе, вы можете использовать dpkg для этого. Он предоставляет
простой и эффективный способ управления deb-пакетами в Linux.

![Task 4](/Task4.png)

5. История команд в терминале Ubuntu.
    - Сохранить и выложить историю ваших терминальных команд в Ubuntu.
    - В формате: Файла с ФИО, датой сдачи, номером группы(или потока).

Хранение истории команд в терминале Ubuntu обеспечивается специальным файлом под названием .bash_history.

Данный файл сохраняет список последних выполненных команд,
позволяя пользователям легко получить доступ к ранее введенным командам и повторно использовать их. Файл .bash_history располагается в домашнем каталоге пользователя (~/.bash_history).

Для просмотра истории команд в терминале Ubuntu можно воспользоваться командой history.

Эта команда отображает список выполненных команд, пронумерованных по порядку.

При этом каждая команда представлена своим номером, что позволяет быстро найти нужную команду.

Также возможно использовать сочетание клавиш Ctrl+R для поиска команд в истории. При вводе этого сочетания клавиш пользователь может начать набирать часть команды, и терминал автоматически предложит наиболее подходящую команду из истории.

Для сохранения истории команд в файл можно использовать переменную окружения HISTFILE.

В стандартной конфигурации Ubuntu переменная HISTFILE установлена в значение ~/.bash_history.

Однако пользователь может изменить это значение, например, на
/path/to/my_history_file, чтобы сохранять историю в другом файле.

В файле .bash_history команды сохраняются в простом текстовом формате в виде последовательности строк.

Каждая строка содержит одну команду, записанную в ней в том виде, в котором она была введена пользователем.

Историю команд можно очистить с помощью команды history -c. Эта команда удаляет все команды из истории. После очистки истории команды не удаляются физически из файла .bash_history, а просто перестают отображаться при использовании команды history.

Вижу, что в задании требуется сохранить и выложить историю команд в терминале Ubuntu.

Однако, из-за соображений конфиденциальности, сохранение и предоставление моего личного файла .bash_history невозможно. Каждый пользователь Ubuntu имеет свой уникальный .bash_history, в котором содержатся его персональные команды.

Учитывая эти ограничения, могу предложить вам следующий вариант.

Мы можем самостоятельно сохранить историю команд в файл, а затем предоставить онлайн ссылку на этот файл.

Для сохранения истории команд в файл можно использовать следующую команду:

    history > history.txt

Эта команда сохраняет историю команд в файл с названием history.txt. После выполнения этой команды в текущем каталоге будет создан файл history.txt, в котором будут записаны все команды из истории терминала.

После сохранения истории команд в файл, вы можете загрузить этот файл на платформу, которая позволяет загружать и пересылать файлы, и предоставить мне ссылку на скачивание.

Таким образом, мы сможем ознакомиться с нашей историей команд в терминале Ubuntu.

[Task 5 - ссылка на историю команд.](/history.txt.txt)

6. Нарисовать [диаграмму](https://github.com/ILYA-NASA/Kennel_account_system/blob/main/UML.drawio), в которой есть класс родительский класс, домашние
   животные и вьючные животные, в составы которых в случае домашних
   животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные
   войдут: Лошади, верблюды и ослы).

![UML](https://user-images.githubusercontent.com/99810114/221403005-bfe39717-2d41-431d-bc03-f78a1aeb76df.jpg)

7. В подключенном MySQL репозитории создать базу данных “Друзья
   человека”

```sql
CREATE DATABASE Human_friends;
```

8. Создать таблицы с иерархией из диаграммы в БД

```sql
USE Human_friends;
CREATE TABLE animal_classes
(
	Id INT AUTO_INCREMENT PRIMARY KEY,
	Class_name VARCHAR(20)
);

INSERT INTO animal_classes (Class_name)
VALUES ('вьючные'),
('домашние');


CREATE TABLE packed_animals
(
	  Id INT AUTO_INCREMENT PRIMARY KEY,
    Genus_name VARCHAR (20),
    Class_id INT,
    FOREIGN KEY (Class_id) REFERENCES animal_classes (Id) ON DELETE CASCADE ON UPDATE CASCADE
);

INSERT INTO packed_animals (Genus_name, Class_id)
VALUES ('Лошади', 1),
('Ослы', 1),
('Верблюды', 1);

CREATE TABLE home_animals
(
	  Id INT AUTO_INCREMENT PRIMARY KEY,
    Genus_name VARCHAR (20),
    Class_id INT,
    FOREIGN KEY (Class_id) REFERENCES animal_classes (Id) ON DELETE CASCADE ON UPDATE CASCADE
);

INSERT INTO home_animals (Genus_name, Class_id)
VALUES ('Кошки', 2),
('Собаки', 2),
('Хомяки', 2);

CREATE TABLE cats
(
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(20),
    Birthday DATE,
    Commands VARCHAR(50),
    Genus_id int,
    Foreign KEY (Genus_id) REFERENCES home_animals (Id) ON DELETE CASCADE ON UPDATE CASCADE
);
```

9. Заполнить низкоуровневые таблицы именами(животных), командами
   которые они выполняют и датами рождения

```sql
INSERT INTO cats (Name, Birthday, Commands, Genus_id)
VALUES ('Пупа', '2011-01-01', 'кс-кс-кс', 1),
('Олег', '2016-01-01', "отставить!", 1),
('Тьма', '2017-01-01', "", 1);

CREATE TABLE dogs
(
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(20),
    Birthday DATE,
    Commands VARCHAR(50),
    Genus_id int,
    Foreign KEY (Genus_id) REFERENCES home_animals (Id) ON DELETE CASCADE ON UPDATE CASCADE
);
INSERT INTO dogs (Name, Birthday, Commands, Genus_id)
VALUES ('Дик', '2020-01-01', 'ко мне, лежать, лапу, голос', 2),
('Граф', '2021-06-12', "сидеть, лежать, лапу", 2),
('Шарик', '2018-05-01', "сидеть, лежать, лапу, след, фас", 2),
('Босс', '2021-05-10', "сидеть, лежать, фу, место", 2);

CREATE TABLE hamsters
(
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(20),
    Birthday DATE,
    Commands VARCHAR(50),
    Genus_id int,
    Foreign KEY (Genus_id) REFERENCES home_animals (Id) ON DELETE CASCADE ON UPDATE CASCADE
);
INSERT INTO hamsters (Name, Birthday, Commands, Genus_id)
VALUES ('Малой', '2020-10-12', '', 3),
('Медведь', '2021-03-12', "атака сверху", 3),
('Ниндзя', '2022-07-11', NULL, 3),
('Бурый', '2022-05-10', NULL, 3);

CREATE TABLE horses
(
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(20),
    Birthday DATE,
    Commands VARCHAR(50),
    Genus_id int,
    Foreign KEY (Genus_id) REFERENCES packed_animals (Id) ON DELETE CASCADE ON UPDATE CASCADE
);
INSERT INTO horses (Name, Birthday, Commands, Genus_id)
VALUES ('Гром', '2020-01-12', 'бегом, шагом', 1),
('Закат', '2017-03-12', "бегом, шагом, хоп", 1),
('Байкал', '2016-07-12', "бегом, шагом, хоп, брр", 1),
('Молния', '2020-11-10', "бегом, шагом, хоп", 1);

CREATE TABLE donkeys
(
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(20),
    Birthday DATE,
    Commands VARCHAR(50),
    Genus_id int,
    Foreign KEY (Genus_id) REFERENCES packed_animals (Id) ON DELETE CASCADE ON UPDATE CASCADE
);
INSERT INTO donkeys (Name, Birthday, Commands, Genus_id)
VALUES ('Первый', '2019-04-10', NULL, 2),
('Второй', '2020-03-12', "", 2),
('Третий', '2021-07-12', "", 2),
('Четвертый', '2022-12-10', NULL, 2);

CREATE TABLE camels
(
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(20),
    Birthday DATE,
    Commands VARCHAR(50),
    Genus_id int,
    Foreign KEY (Genus_id) REFERENCES packed_animals (Id) ON DELETE CASCADE ON UPDATE CASCADE
);
INSERT INTO camels (Name, Birthday, Commands, Genus_id)
VALUES ('Горбатый', '2022-04-10', 'вернись', 3),
('Самец', '2019-03-12', "остановись", 3),
('Сифон', '2015-07-12', "повернись", 3),
('Борода', '2022-12-10', "улыбнись", 3);
```

10. Удалив из таблицы верблюдов, т.к. верблюдов решили перевезти в другой
    питомник на зимовку. Объединить таблицы лошади, и ослы в одну таблицу.

```sql
SET SQL_SAFE_UPDATES = 0;
DELETE FROM camels;

SELECT Name, Birthday, Commands FROM horses
UNION SELECT  Name, Birthday, Commands FROM donkeys;
```

11. Создать новую таблицу “молодые животные” в которую попадут все
    животные старше 1 года, но младше 3 лет и в отдельном столбце с точностью
    до месяца подсчитать возраст животных в новой таблице

```sql
CREATE TEMPORARY TABLE animals AS
SELECT *, 'Лошади' as genus FROM horses
UNION SELECT *, 'Ослы' AS genus FROM donkeys
UNION SELECT *, 'Собаки' AS genus FROM dogs
UNION SELECT *, 'Кошки' AS genus FROM cats
UNION SELECT *, 'Хомяки' AS genus FROM hamsters;

CREATE TABLE yang_animal AS
SELECT Name, Birthday, Commands, genus, TIMESTAMPDIFF(MONTH, Birthday, CURDATE()) AS Age_in_month
FROM animals WHERE Birthday BETWEEN ADDDATE(curdate(), INTERVAL -3 YEAR) AND ADDDATE(CURDATE(), INTERVAL -1 YEAR);

SELECT * FROM yang_animal;
```

12. Объединить все таблицы в одну, при этом сохраняя поля, указывающие на
    прошлую принадлежность к старым таблицам.

```sql
SELECT h.Name, h.Birthday, h.Commands, pa.Genus_name, ya.Age_in_month
FROM horses h
LEFT JOIN yang_animal ya ON ya.Name = h.Name
LEFT JOIN packed_animals pa ON pa.Id = h.Genus_id
UNION
SELECT d.Name, d.Birthday, d.Commands, pa.Genus_name, ya.Age_in_month
FROM donkeys d
LEFT JOIN yang_animal ya ON ya.Name = d.Name
LEFT JOIN packed_animals pa ON pa.Id = d.Genus_id
UNION
SELECT c.Name, c.Birthday, c.Commands, ha.Genus_name, ya.Age_in_month
FROM cats c
LEFT JOIN yang_animal ya ON ya.Name = c.Name
LEFT JOIN home_animals ha ON ha.Id = c.Genus_id
UNION
SELECT d.Name, d.Birthday, d.Commands, ha.Genus_name, ya.Age_in_month
FROM dogs d
LEFT JOIN yang_animal ya ON ya.Name = d.Name
LEFT JOIN home_animals ha ON ha.Id = d.Genus_id
UNION
SELECT hm.Name, hm.Birthday, hm.Commands, ha.Genus_name, ya.Age_in_month
FROM hamsters hm
LEFT JOIN yang_animal ya ON ya.Name = hm.Name
LEFT JOIN home_animals ha ON ha.Id = hm.Genus_id;
```

13. Создать [класс с Инкапсуляцией методов и наследованием по диаграмме](https://github.com/ILYA-NASA/Kennel_account_system/tree/main/System/src/Model).
14. Написать [программу, имитирующую работу реестра домашних животных](https://github.com/ILYA-NASA/Kennel_account_system/tree/main/System/src).
    В программе должен быть реализован следующий функционал:  
     14.1 Завести новое животное  
     14.2 определять животное в правильный класс  
     14.3 увидеть список команд, которое выполняет животное  
     14.4 обучить животное новым командам  
     14.5 Реализовать навигацию по меню
15. Создайте [класс Счетчик](https://github.com/ILYA-NASA/Kennel_account_system/blob/main/System/src/Controller/Counter.java), у которого есть метод add(), увеличивающий̆
    значение внутренней̆ int переменной̆ на 1 при нажатии “Завести новое
    животное” Сделайте так, чтобы с объектом такого типа можно было работать в
    блоке try-with-resources. Нужно бросить исключение, если работа с объектом
    типа счетчик была не в ресурсном try и/или ресурс остался открыт. Значение
    считать в ресурсе try, если при заведении животного заполнены все поля.

![Program](https://user-images.githubusercontent.com/99810114/221417421-93de1f4c-ad41-4f7e-a45d-edd5ec72f1d3.jpg)

![image](https://user-images.githubusercontent.com/99810114/222143283-7ec9e203-2a23-4cf4-81b8-b97a159cdc79.png)
