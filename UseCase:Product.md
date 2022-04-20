Use Case: Product

@startuml

left to right direction

(Просмотр характеристик товара) as a

(Просмотр товара) as b


(Просмотр категорий) as c

(Просмотр подкатегорий) as d

(Поиск товара) as e

(Просмотр товара на наличие) as f



Actor as z

z -- a

z -- b

z -- c

z -- d

z -- e

z -- f


b <.. (по скидке): extend

b <.. (по цене): extend


(Добавление товара) as aa

(Удаление товара) as bb

(Добавление категории) as cc

(Удаление категории) as dd

(Добавление характеристик товара) as ee

(Удаление характеристик товара) as ff

(Изменение характеристик товара) as gg


Admin as zz


z <|-right-- zz

 
zz -- aa

zz -- bb

zz -- cc

zz-- dd

zz -- ee

zz -- ff

zz -- gg


zz -- f

e <.. (по тегу): extend

e <.. (по названию): extend

e <.. (по категории): extend

e <.. (по подкатегории): extend

@enduml

![image](https://user-images.githubusercontent.com/104089098/164281154-fee4e49c-ed5c-4640-99bd-2fc428be2724.png)
