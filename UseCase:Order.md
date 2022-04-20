Use Case: Order


@startuml

left to right direction

(Просматривать информацию о заказе) as a

(Изменять заказ) as b

(Создать заказ) as c

(Отменить заказ) as d

Actor as z

Admin as zz


z -- a

z -- b

z -- c

z -- d


zz -- a

zz -- d

@enduml

![image](https://user-images.githubusercontent.com/104089098/164283060-20baba2d-938e-4137-b07a-3a828b3d6b6e.png)
