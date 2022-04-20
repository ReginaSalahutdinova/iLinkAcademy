UseCase:Auth

@startuml

(вход в аккаунт) as a
(выход из аккаунта) as b
left to right direction
:Actor:-- a
:Actor:--b

(По номеру телефона) as z
(По  VKID) as zz
(По SberID) as zzz

a <.. z:extend

z ..> (ввод номера телефона) : include

z ..> (подтверждение кодом): include


a <.. zz:extend

zz ..> (ввод номера телефона или почты) : include
zz ..> (подтвердить код) : include
zz ..> (выбор существующего аккаунта) : include

a <.. zzz:extend

(ввод номера телефона) as h
(подтверждение кодом) as hh
zzz ..> h : include
zzz ..> hh: include
zzz ..> (вход через существующее приложение Sberbank) : include
@enduml
