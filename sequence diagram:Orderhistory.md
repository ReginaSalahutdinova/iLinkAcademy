Диаграмма последовательности: просмотр истории заказов

@startuml

Actor Actor as z

participant Frontend as f

participant "Backend\n(Gateway)" as g

participant "Backend\n(Profile)" as p

participant "Backend\n(Auth)" as a

participant "Backend\n(Order)" as o


z->f: запрос на просмотр истории заказов

f->g: запрос на просмотр истории заказов

g->p: запрос на просмотр истории заказов


p->a: проверка токена авторизации

a-> a: верификация токена


alt авторизация не пройдена


a --> p: ошибка авторизации
    
p --> g: сообщение об ошибке

f <-- g: сообщение об ошибке


else авторизация прошла успешно



a --> p: ответ о пройденной авторизации

p-> o: запрос на просмотр

o-> o: формирование списка из БД

o--> p: передача списка заказов

p--> g: передача списка заказов

g--> f: передача списка заказов

f-->z: отображение списка заказов пользователя

end

@enduml

![image](https://user-images.githubusercontent.com/104089098/164286235-89860f17-060b-43d6-9ad0-464e963c3415.png)
