# Use Сase: Самокат


@startuml 

left to right direction

(Авторизация) as a 

(Оформление заказа) as b 

(Просмотр личного кабинета) as c 

(Просмотр статей) as d

(Просмотр информации товара) as dd 

(Просмотр товаров по категориям) as e 

(Корзина) as f 

(Просмотр информации по доставке) as g 


Actor as z

z -- a

z -- b

z -- c

z -- d

z -- dd

z -- e

z -- f

z -- g


a <.. (номер телефона): extend

a <.. (VKID): extend

a <.. (SberPay): extend

b ..> (Оплата): include

b <..  (введение промокода): extend

 
f <.. (удаление товара): extend

f <..(добавление товара): extend

f <..(Изменение колличества товаров): extend

f <..(просмотр товаров): extend



c <.. (Просмотр списка заказов): extend

c <.. (Просмотр списка адресов): extend

c <.. (Изменение адреса): extend

c <.. (Просмотр персональных скидок/промокодов): extend

c <.. (Просмотр настроек): extend

c <.. (изменение настроек): extend

c <.. (избранное): extend

c <.. (выход из аккаунта): extend

c <.. (связь с техподдержкой): extend

e <.. (поиск товара): extend

(избранное) <.. (добавить): extend

(избранное) <.. (удалить): extend

(избранное) <.. (просмотреть список): extend


(изменение настроек) <.. (изменить имя): extend

(изменение настроек) <.. (сохранить почту): extend

(изменение настроек) <.. (привязать аккаунт): extend

(изменение настроек) <.. (вкл/выкл пуш-уведомления): extend

(изменение настроек) <.. (вкл/выкл новости, акции): extend

@enduml
![celoe](https://user-images.githubusercontent.com/104089098/164276449-a19c398b-3ed6-4eee-aea6-595007be7aee.jpg)

