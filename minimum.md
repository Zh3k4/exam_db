## 1. Дайте определение понятию "система управления базами данных". Расскажите, из каких частей состоит современная СУБД, и для чего они предназначены.

**СУБД** - совокупность языковых и программных средств, предназначенных для создания, ведения и совместного использования БД многими пользователями.

### Составные части современной БД

ЯОД – язык описания данных, ЯМД – язык манипуляции данными.

С помощью средств создания БД проектировщик, используя ЯОД, переводит логическую модель БД в физическую структуру, а на ЯМД разрабатывает программы, реализующие основные операции с данными.

При проектировании привлекаются визуальные средства, т.е. объекты, и программа-отладчик, с помощью которой тестируются отдельные блоки программы управления конкретной БД.

Средства работы с данными предназначены для пользователя БД. Они позволяют установить удобный интерфейс с пользователем, производить операции с данными БД.

Сервисные средства позволяют при проектировании БД привлечь к работе другие системы.

## 2. Перечислите и опишите функции «систем управления базами данных (СУБД)».

### Непосредственное управление данными во внешней памяти
Обеспечение необходимых структур внешней памяти для хранения данных, непосредственно входящих в БД.
Механизм работы скрыт от пользователя.

### Управление буферами оперативной памяти
СУБД обычно работают с БД значительного размера. Практически единственным способом реального увеличения этого объема является буферизация данных в оперативной памяти. В развитых СУБД поддерживается собственный набор буферов оперативной памяти с собственной дисциплиной замены буферов.

### Управление транзакциями
**Транзакция** – это последовательность операций над БД, рассматриваемых СУБД как единое целое. Либо транзакция успешно выполняется, и СУБД фиксирует изменения БД во внешней памяти, либо ни одно из этих изменений никак не на БД.

Каждая транзакция начинается при целостном состоянии БД и оставляет это состояние целостным после завершения.

### Журнализация
Одним из основных требований к СУБД является надежность хранения данных во внешней памяти.

**Надежность хранения** – СУБД должна быть в состоянии восстановить последнее согласованное состояние БД после сбоя. Наиболее распространенным методом поддержания избыточной информации является ведение журнала изменений БД.

**Журнал** – это особая часть БД, недоступная пользователям СУБД, в которую поступают записи обо всех изменениях основной части БД.

## 3. Перечислите и опишите типы данных Microsoft Access.

### Текстовый.
Хранит комбинации символов в пределах 255 знаков.

### Поле МЕМО.
Хранит комбинации символов в пределах, примерно, 65 тысяч знаков.

Этот тип данных отличается от типа "Текстовый" тем, что в таблице даются не сами данные, а ссылки на блоки данных, хранящиеся отдельно. За счет этого ускоряется обработка таблиц (сортировка, поиск и т.п.).

Поле типа MEMO не может быть ключевым или проиндексированным.

### Числовой.
Данные, используемые для математических вычислений, за исключением финансовых расчетов.

### Дата/время.
Значения дат и времени.

### Денежный.
Используется для денежных значений и для предотвра-щения округления во время вычислений.

### Счетчик.
Автоматическая вставка уникальных последовательных (увеличивающихся на 1) или случайных чисел при добавлении записи.

### Логический.
Данные, принимающие только одно из двух возможных значений, таких, как «Да/Нет», «Истина/Ложь», «Вкл./Выкл.».

### Поле объекта OLE.
Объекты OLE. Такие, как документы Microsoft Word, электронные таблицы Microsoft Excel, рисунки, звукозапись, другие (ограничивается объемом диска).

### Гиперссылка.
Гиперссылка может указывать на расположение файла на локальном компьютере либо адреса URL.

### Мастер подстановок.
Создает поле, позволяющее выбрать значение из другой таблицы или из списка значений, используя поле со списком.

## 4. Дайте определение «отчет базы данных». Охарактеризуйте типы отчетов.

**Отчет** – это форматированное представление данных, которое выводится на экран, на печать или файл.

Они позволяют извлечь из базы нужные сведения и представить их в виде, удобном для восприятия. Данные в отчете редактировать нельзя. Готовый отчет выводит информацию, разбитую на страницы и подготовленную к печати. Отчеты создаются специальными наборами компонентов.

Типы отчетов:

- Простой отчет. Отчет содержащий набор данных одной таблицы или запроса. 

- Отчет главный-детальный. Данный отчет воспроизводит данные из одной записи главной таблицы и все записи связанной с ней дочерней таблицы.

- Группирующий отчет. Вся информация разделяется на группы, объединенных каким-то общим признаком.

## 5. Раскройте следующие понятия: набор данных, курсор набора данных, текущая запись.

**Набор данных** – это множество записей из одной или нескольких    таблиц базы данных.

**Курсор набора данных** – указатель текущей записи в конкретном наборе данных.

**Текущая запись** – это та запись, над которой в данный момент времени можно выполнять какие-либо операции.

<!--
Пользователь может перемещаться к началу и концу набора записей, к следующей или предыдущей записи по отношению к текущей, с помощью компонента TDBNavigator и встроенных возможностей компонента TDBGrid.
-->

## 6. Перечислите свойства строк и столбцов реляционной БД.

Столбцы и строки должны иметь следующие свойства:

- всякому столбцу таблицы присвоено имя, которое должно быть уникальным для этой таблицы;

- столбцы таблицы упорядочиваются слева направо;

- в поле на пересечении строки и столбца любой таблицы всегда имеется только одно значение данных, и никогда не должно быть множества значений; 

- все строки таблицы обязательно отличаются друг от друга хотя бы    единственным значением, что позволяет идентифицировать любую строку    такой таблицы;

- строки таблицы не упорядочены;

- всем строкам таблицы соответствует одно и то же множество столбцов;

- при выполнении операций с таблицей ее строки и столбцы можно обрабатывать в любом порядке безотносительно к их информационному    содержанию.

## 7. Приведите и охарактеризуйте основные операции над данными двух таблиц.

### Ввод записей.
Данные сначала вводятся в основную таблицу, а потом – в дополнительную.
В процессе заполнения основной таблицы контроль значений полей связи ведется как контроль обычного ключа.
Заполнение полей дополнительной таблицы контролируется на предмет совпадения со значениями полей основной таблицы.

### Модификация записей.
Изменение содержимого полей связанных записей, не относящихся к полям связи, должно происходить обычным образом. Но при редактировании полей связи дополнительной таблицы очевидным требованием является то, чтобы новое значение поля связи совпадало с соответствующим значением какой-либо записи основной таблицы.

### Удаление записей.
Удаление записей дополнительной таблицы происходит практически бесконтрольно.

## 8. Охарактеризуйте вложенный подзапрос.

**Вложенный подзапрос** – это подзапрос, заключенный в круглые скобки и вложенный в фразу WHERE. Вложенный подзапрос может содержать в своей фразе WHERE другой вложенный подзапрос.

```sql
SELECT ... FROM ...
WHERE (
	SELECT ... FROM ...
	WHERE (...)
)
```

## 9. Перечислите и опишите команды внесения изменения в БД и извлечения данных.

- `SELECT` - вывод информации из таблицы.

	```sql
	SELECT столбцы FROM таблица
	WHERE условие
	```

- `INSERT` - вставка строк в таблицу.

	```sql
	INSERT INTO таблица (столбцы)
	VALUES (значения)
	```

- `UPDATE` - обновлени данных в таблице.

	```sql
	UPDATE таблица
	SET столбец = значение
	WHERE условие
	```

- `DELETE` - удаление данных их таблицы.

	```sql
	DELETE FROM таблица
	WHERE условие
	```

## 10. Расскажите о функциях администратора БД

- Анализ предметной области: описание предметной области. выявление ограничений целостности, определение статуса (доступности, секретности) данных, определение потребностей пользователей.

- Проектирование структуры БД: описание информационного содержания и внутренней структуры БД.

- Задание ограничений целостности при описании структуры БД

- Первоначальная загрузка и ведение БД

- Защита данных

- Обеспечение восстановления БД:
  - разработка организационных средств архивирования и принципов восстановления БД;
  - разработка дополнительных программных средств и технологических процессов восстановления БД после сбоев.
  
- Анализ обращений пользователей: сбор статистики по характеру запросов, времени их выполнения.

- Анализ эффективности функционирования БД; анализ показателей функционирования БД, планирование реструктуризации.

- Работа с конечными пользователями:
  - сбор информации об изменении предметной области, об оценке работы БД,
  - обучение и консультирование пользователей.
  
- Подготовка и поддержание системных средств: анализ существующих на рынке программных средств и возможность их использования, проверка работоспособности закупаемых программных средств.

- Организационно-методическая работа по проектированию БД:
  - выбор или создание методики проектирования БД, определение целей и направления развития системы в целом; планирование этапов развития БД;
  - обеспечение возможностей комплексной отладки множества приложений, взаимодействуюших с БД и тд.
