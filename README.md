![Неудачный студент](https://user-images.githubusercontent.com/20025263/111709300-6781ee00-8858-11eb-9cad-cc08dc4ddb9c.png)
# 1.4_v7
Подготовка к демо 2021 вариант 7

# Меню навигации
- [Смотреть исходники готового решения](https://github.com/LackyCraft/1.4_v5/tree/main/Сессия)
 - **Учебные материалы:**
     - **Текстовые пособия:**
       - [Руководство по WPF (mateint)](https://metanit.com/sharp/wpf/)
       - [Полное руководство уководство по WPF (professorweb)](https://professorweb.ru/my/WPF/base_WPF/level1/info_WPF.php)
     - **Видео пособия:**
       - [Первые шаги в WP (разметка)](https://youtube.com/playlist?list=PL0lO_mIqDDFVI0xwaYbm7h9ewYu5hftfA)
       - [Основы XAML (1-7 видео)](https://vk.com/video323169425_456239587)

# Описание задания
<details>
  <summary>Сессия 1 ✅</summary>
 
- Проектирование требований
- Спецификации к UseCase
- Восстановление базы данных из скрипта
- Импорт данных
 
✅ <strong>Создать диаграмму прицидентов</strong> (критерии: имеются актеры "Аналитик", "Менеджер", "Мастер производства", "Сотрудник склада", сохранена, как pdf название: UseCase_XX, где XX - номер вашего рабочего места)
  <br>
✅ <strong>База данных:</strong> база данных восстановлена из скрипта верно импортированы таблицы: material, supplier, materialsuplier**
  <br>
</details>

<details>
  <summary>Сессия 2 (Разработка прилоежния) ✅</summary>
 
- Проектирование требований
- Спецификации к UseCase
- Восстановление базы данных из скрипта
- Импорт данных
 
### Главное меню
✅ Пагинация и главное меню
<br>
 - [+]наименование, количество продаж за год, размер скидки, телефон и тип агента.
 - [+]Вывод должен осуществляться постранично (по 10 записей на страницу).
 - [+]Для удобства навигации по страницам необходимо вывести список их номеров (как на макете) с возможностью перехода к выбранной странице, а также предусмотреть переходы к предыдущей и следующей страницам. ![image](https://user-images.githubusercontent.com/20025263/165804149-d9e6f2d5-c6ca-4117-ab99-564ea08cffcd.png)
 - [+] Количество продаж вычисляется как общее количество проданных единиц продукции за последний год (365 дней).
Размер скидки вычисляется на основании успешности организации продаж за весь период. Механизм 
подсчета скидок для агента исходя из общей суммы реализации продукции: [0-10000) -> 0%, [10000-50000) -> 5%, [50000-150000) -> 10%, [150000-500000) -> 20%, [500000-...] -> 25%.

✅ Сортировка
<br>
 - [+]Сортировка по: (по возрастанию и убыванию) по следующим параметрам: наименование, размер скидки и приоритет агента

✅ Фильтрация
<br>
 - [+]Фильтрация по: по типу агента. 
 - [+]Первым элементом в выпадающем списке должен быть “Все типы”, при выборе которого настройки фильтра сбрасываются.

✅ Поиск
<br>
[+] Пользователь должен иметь возможность искать агентов, используя поисковую строку. Поиск должен 
осуществляться по наименованию и контактным данным (email и номер телефона агента).
Поиск, сортировка и фильтрация должны происходить в реальном времени, без необходимости нажатия 
кнопки “найти”/”отфильтровать” и т.п. Фильтрация и поиск должны применяться совместно. Параметры 
сортировки, выбранные ранее пользователем, должны сохраняться и во время фильтрации с поиском.
<br>
 
✅ Строка состояния
 <br>
 - [+]В верхней части окна необходимо показывать количество выведенных данных и общее количество записей в базе. Например, 155 из 237.
 <br>
 
✅ Зависимость цвета от количества
<br>
 - [+]Агнеты со скидкой 25% и выше должны быть выделены светло-зеленым цветом.
<br>
 
✅ Изменение
<br>
[+]Необходимо добавить возможность изменения приоритета для нескольких выбранных агентов. Для этой 
цели реализуйте возможность выделения сразу нескольких элементов в списке агентов, после чего 
должна появиться кнопка “Изменить приоритет на ...”. При нажатии на кнопку необходимо отобразить 
модальное окно с возможностью ввода числового значения, на которое и будет изменен приоритет 
агентов. По умолчанию в поле должно быть введено максимальное значение среди всех приоритетов 
выбранных агентов. После нажатия кнопки “Изменить” приоритет выделенных агентов должен быть 
изменен в базе данных, а также обновлен в интерфейсе.
<br>

### Добавление/редактирование агентов
<br>
 - [-]Форма редакитрвоания и создания заявок
На форме должны быть предусмотрены следующие поля: наименование, тип агента (выпадающий 
список), приоритет, логотип компании, адрес, ИНН, КПП, имя директора, телефон и email компании.
 - [-]При открытии формы для редактирования все поля выбранного объекта должны быть подгружены в соответствующие поля из базы данных, а таблица заполнена актуальными значениями.
 - [-]Приоритет агента и количество продукции должны быть целыми неотрицательными числами.
 - [-]Пользователь может добавить/заменить логотип агента
 - [-]Для того чтобы администратор случайно не изменял несколько агентов, предусмотрите невозможность открытия более одного окна редактирования.
       - [-]В окне редактирования агента должна присутствовать кнопка “Удалить”, которая удаляет агента из базы данных.
       - [-]Если у агента есть информация о точках продаж агентов или история изменения приоритета, то эта информация должна быть удалена вместе с агентом. 
	   - [-]Но если у агента есть информация о реализации продукции, то удаление агента из базы данных должно быть запрещено.
	   - [-]После удаления агента система должна сразу вернуть пользователя обратно к списку агентов.
	   - [-]После редактирования/добавления/удаления агента данные в окне списка агентов должны быть обновлены, при изменении информации о реализации продукции, необходимо пересчитывать скидку
<br>

### Разработка тестовых сценариев (Test-cases)
<br>
Для выполнения процедуры тестирования удаления агентов Вам нужно описать пять сценариев. Удаление 
может быть выполнимо, а может быть отклонено согласно требованиям предметной области. 
Необходимо, чтобы варианты тестирования демонстрировали различные исходы работы алгоритма. Для 
описания тестовых сценариев в ресурсах предоставлен шаблон testing-template.docx.
<br>

### Создание руководства пользователя
<br>
Вам необходимо разработать руководство пользователя для вашего настольного приложения, которое 
описывает последовательность действий для выполнения всех функций вашей системы.
При подготовке документации старайтесь использовать живые примеры и скриншоты вашей системы для 
более наглядного пояснения шагов работы с различным функционалом.
Обратите внимание на оформление документа: оформите титульный лист, используйте автоматическую 
нумерацию страниц, разделите руководство на подразделы и сформируйте оглавление, используйте 
ссылки на рисунки, нумерованные и маркированные списки для описания шагов и т.д.
 - [-]Файл сохранен в WORD в соответсвии с названием шаблона: "Руководство пользователя_XX", где XX - номер вашего рабочего места.
<br>

</details>

# Скриншоты готового решения для компании «Глазки»
## Главное меню
![image](https://user-images.githubusercontent.com/20025263/166502691-8fb0ffa3-b9f0-47a3-b6aa-fca2952cfb50.png)
### Изменение приоритета
![image](https://user-images.githubusercontent.com/20025263/166502886-8b36ed10-ac28-4866-ba26-ec20591a662e.png)
### Пагинация
![image](https://user-images.githubusercontent.com/20025263/166503091-d42ab41d-51af-4e2c-bb52-8c7ec0eaad68.png)

## Дабавление 
![image](https://user-images.githubusercontent.com/20025263/166569057-3b5c6815-b6cb-48e3-a314-b2a2884f7459.png)

## Редактирование 
![image]()

