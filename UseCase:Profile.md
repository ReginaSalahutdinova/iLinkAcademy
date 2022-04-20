Use Case: Profile

@startuml

left to right direction

(Привязать аккаунт VKID) as a

(Просмотр информации) as b

(Редактирование информации) as c

(Удаление информации) as d

(Добавление информации) as e

(Изменение настроек) as f

(Избранное) as g


Actor -- a

Actor -- b

Actor -- c

Actor -- d

Actor -- e

Actor -- f

Actor -- g


b <.. (о пользователе): extend

b <.. (о заказе): extend

b <.. (об адресах): extend

b <.. (о персональных скидках/промокодах): extend


(о пользователе) as oo

(об адресах) as o

c <.. oo: extend

c <.. o: extend


oo <.. (почта) : extend

oo <.. (имя) : extend


(о пользователе) as r

(об адресах) as rr

d <.. r: extend

d <.. rr: extend


(об адресах) as hh

e <.. hh :extend


f <.. (вкл/выкл пуш-уведомлений): extend

f <.. (вкл/выкл акций, скидок): extend



g <.. (добавить) : extend

g <.. (удалить) : extend

g <.. (просмотреть) : extend

@enduml


![image](https://user-images.githubusercontent.com/104089098/164281792-6f5ff7f7-7424-4250-b818-df93a353b74d.png)


