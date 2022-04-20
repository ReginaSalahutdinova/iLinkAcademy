Use Case: Sale

@startuml

left to right direction


(Просмотр персональной скидки) as a

(Просмотр скидки на товары) as b

(Просмотр промокода) as c

(Создание скидки) as d

(Удаление скидки) as e

(Редактирование скидки) as f

(Создание промокода) as g

(Удаление промокода) as h



Actor as z

Admin as zz


z -- a

z -- b

z -- c


zz -- d

zz -- b

zz -- e

zz -- f

zz -- g

zz -- h

@enduml



![image](https://user-images.githubusercontent.com/104089098/164283632-a66c2c04-365f-4656-b49e-fdba8aa6f45f.png)
