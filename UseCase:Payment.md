Use Case: Payment


@startuml

left to right direction

(Оплатить заказ) as a

(Просмотреть информацию об оплате заказа) as b


Actor as z

Admin as zz



z — a

zz — b


a <.. (создать новую карту): extend

a <.. (выбрать имеющуюся карту): extend


@enduml

![image](https://user-images.githubusercontent.com/104089098/164282709-df6625fb-e927-4dd8-90a8-c9bb46c2c5be.png)
