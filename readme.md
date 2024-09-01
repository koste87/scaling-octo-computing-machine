# Product and Category Management

## Описание

Этот проект демонстрирует базовые классы для управления продуктами и категориями в системе управления товарами.
Классы `Product` и `Category` позволяют создавать объекты продуктов и категорий, а также отслеживать количество
продуктов и категорий в системе.

## Классы

### `Product`

Класс `Product` представляет собой продукт с следующими атрибутами:

- `name` (str): Название продукта.
- `description` (str): Описание продукта.
- `price` (float): Цена продукта.
- `quantity` (int): Количество продукта на складе.

**Методы:**

- `__init__(self, name, description, price, quantity)`: Конструктор для создания нового объекта продукта.

### `Category`

Класс `Category` представляет собой категорию товаров и содержит:

- `name` (str): Название категории.
- `description` (str): Описание категории.
- `list_product` (list): Список продуктов в данной категории.
- `category_count` (int): Общее количество категорий.
- `product_count` (int): Общее количество продуктов во всех категориях.

**Методы:**

- `__init__(self, name, description, list_product)`: Конструктор для создания новой категории и добавления продуктов в
  нее.

## Пример использования

```python
from src.category import Category
from src.product import Product

if __name__ == "__main__":
    product1 = Product("Samsung Galaxy S23 Ultra", "256GB, Серый цвет, 200MP камера", 180000.0, 5)
    product2 = Product("Iphone 15", "512GB, Gray space", 210000.0, 8)
    product3 = Product("Xiaomi Redmi Note 11", "1024GB, Синий", 31000.0, 14)

    print(product1.name)
    print(product1.description)
    print(product1.price)
    print(product1.quantity)

    print(product2.name)
    print(product2.description)
    print(product2.price)
    print(product2.quantity)

    print(product3.name)
    print(product3.description)
    print(product3.price)
    print(product3.quantity)

    category1 = Category("Смартфоны",
                         "Смартфоны, как средство не только коммуникации, но и получения дополнительных"
                         " функций для удобства жизни",
                         [product1, product2, product3])

    print(category1.name == "Смартфоны")
    print(category1.description)
    print(len(category1.list_product))
    print(category1.category_count)
    print(category1.product_count)

    product4 = Product(r"55\" QLED 4K", "Фоновая подсветка", 123000.0, 7)
    category2 = Category("Телевизоры",
                         "Современный телевизор, который позволяет наслаждаться просмотром,"
                         " станет вашим другом и помощником",
                         [product4])

    print(category2.name)
    print(category2.description)
    print(len(category2.list_product))
    print(category2.list_product)

    print(Category.category_count)
    print(Category.product_count)
Установка
Склонируйте репозиторий:

git clone <URL>
Перейдите в каталог проекта:

cd <project-directory>
Установите зависимости (если есть):

pip install -r requirements.txt
Запуск
Запустите основной скрипт для создания и управления продуктами и категориями:

python src/main.py
Лицензия
Этот проект лицензируется на условиях MIT License. См. файл LICENSE для подробностей.


Не забудьте заменить `<URL>` и `<project-directory>` на актуальные значения для вашего проекта.