# Применение
Сервис используется для добавление данных о заказе в базу данных компании.

# Используемый метод
#Add - метод используется для добавление нового заказа в БД
#Get - метод используется для получения идентификатора созданного заказа 

# Добавление нового заказа (#Add)
Вызов
| Поле | Название | Доп. описание | Тип поля | Обязательность | Маппинг |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| CUSTOMERID | Идентификатор покупателя | - | string | Y | customer.id |
| ORDDATE | Дата оформления заказа | Формат YYYY.MM.DD HH:MM:SS | timestamp | Y | order.date |
| PRODUCTAMOUNT | Количество товаров в заказе | - | number | Y | product.amount |
| PRODUCTNAME | Название товара | - | string | Y | product.name |
| PAYMENTWAY | Способ оплаты | - | string | Y | order.payment |
| DELIVERY | Способ получения | - | string | Y | order.wayOfGet |
| ADDRESS | Адрес доставки | - | string | Y | order.address / client.address |
| RECIEVER | Получатель | - | string | Y | order.reciever |
Ответ
| Поле | Название | Доп. описание | Тип поля | Обязательность | Маппинг |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| ORDERID | Идентификатор заказа | - | string | Y | order.number |

# Загрузка списка заказов клиента (#Get)
Вызов
| Поле | Название | Доп. описание | Тип поля | Обязательность | Маппинг |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| CUSTOMERID | Идентификатор покупателя | - | string | Y | customer.id |


Ответ
| Поле | Название | Доп. описание | Тип поля | Обязательность | Маппинг |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| ORDERID | Идентификатор заказа | - | string | Y | order.number |
| ORDENDDATE | Дата выполнения заказа | Формат YYYY.MM.DD HH:MM:SS | timestamp | N | order.dateEnd |
| ORDSTATUS | Статус заказа | - | string | Y | order.status |
| ORDDATE | Дата оформления заказа | Формат YYYY.MM.DD HH:MM:SS | timestamp | Y | order.date |
| PRODUCTAMOUNT | Количество товаров в заказе | - | number | Y | product.amount |
| PRODUCTNAME | Название товара | - | string | Y | product.name |
| PAYMENTWAY | Способ оплаты | - | string | Y | order.payment |
| DELIVERY | Способ получения | - | string | Y | order.wayOfGet |
| ADDRESS | Адрес доставки | - | string | Y | order.address / client.address |
| RECIEVER | Получатель | - | string | Y | order.reciever |
