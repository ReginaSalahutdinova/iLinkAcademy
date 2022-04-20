Диаграмма последовательности: просмотр подробной информации о товаре

@startuml

Actor Actor as z

participant Frontend as f

participant "Backend\n(Gateway)" as g

participant "Backend\n(Product)" as p

participant "Backend\n(Sale)" as s

z -> f: нажимает на товар

f -> g: запрос на товар

g -> p: запрос на товар

p<- p: получение информации о товаре из БД

p -> s: запрос на скидку по товару

s -> s: поиск скидки в БД

p <-- s: передача информации\nо скидке по товару



p --> g: передача информации о товаре

g --> f: передача информации о товаре


f--> z: передача конечной информации о товаре

@enduml

![image](https://user-images.githubusercontent.com/104089098/164285803-445214bd-ead1-4c7d-995c-167dcbcac056.png)
