Задание 1: СТРУКТУРА ПРОЕКТА
Создадим следующую структуру каталогов и файлов:

accounting/
│
├── main.py
├── dirty_main.py          
├── requirements.txt
│
└── application/
    ├── __init__.py
    ├── salary.py
    └── db/


Задание 2: КОД МОДУЛЕЙ

Файл: application/salary.py
from datetime import datetime

def calculate_salary():
    print(f"Выполняется расчёт заработной платы... (дата: {datetime.now().strftime('%Y-%m-%d')})")

Файл: application/db/people.py
from datetime import datetime

def get_employees():
    print(f"Получение списка сотрудников... (дата: {datetime.now().strftime('%Y-%m-%d')})")

Файл: main.py
from datetime import datetime
from application.salary import calculate_salary
from application.db.people import get_employees

if __name__ == '__main__':
    print(f"Запуск программы 'Бухгалтерия' ({datetime.now().strftime('%Y-%m-%d')})")
    get_employees()
    calculate_salary()

Задание 3: ПОЯСНЕНИЯ К КАЖДОЙ СТРОКЕ КОДА
application/salary.py
from datetime import datetime — импортируем класс datetime из стандартного модуля datetime, чтобы получать текущее время.
def calculate_salary(): — объявляем функцию, которая будет "рассчитывать зарплату".
print(...) — выводим сообщение с текущей датой, отформатированной как ГГГГ-ММ-ДД.
application/db/people.py

Аналогично: импортируем datetime, объявляем функцию get_employees, выводим сообщение с датой.
main.py
from datetime import datetime — снова импортируем, чтобы вывести дату при запуске основной программы.
from application.salary import calculate_salary — импортируем функцию из модуля salary.
from application.db.people import get_employees — импортируем функцию из вложенного модуля people.
if __name__ == '__main__': — стандартная конструкция, которая гарантирует выполнение кода только при непосредственном запуске main.py, а не при импорте.

Внутри блока:
Выводим приветственное сообщение с датой.
Вызываем get_employees() → выводит список сотрудников.
Вызываем calculate_salary() → имитирует расчёт ЗП.
Программа соответствует требованиям: импорты корректны, вывод даты присутствует, структура соблюдена.

Задание 4: ФАЙЛ requirements.txt
Выберем интересный и популярный пакет с PyPI. Например, requests — удобная библиотека для HTTP-запросов.

Файл requirements.txt:
requests==2.32.3



