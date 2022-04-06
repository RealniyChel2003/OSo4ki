## Лабораторная работа номер 5

В этой ветке можно найти ansible-файл, который выполняет следующие функции: 

Устанавливает на серверах web1 web2 nginx
На серверах haproxy1, haproxy2 устанавливает и настраивает отказоустойчивую связку HAProxy+Keepalived
На серверах web1, web2 Nginx работает по порту 8080 и отдает кастомную страницу
На серверах с HAProxy ПО обеспечивает балансировку нагрузки серверов web1 и web2 в режиме round-robin.

## Для поднятия машин:

```
vagrant up
```
Запуск сценария:

```
ansible-playbook nginx
```

## Балансировка:

<img src="https://camo.githubusercontent.com/66d0e077c38e3ff231b928e5715934176f9c414ffa0092799dfa35315c3761f0/68747470733a2f2f692e6962622e636f2f4e724335636e532f77656262312e6a7067" >
<img src="https://camo.githubusercontent.com/3e5a3bd939b549d3fc24977aaa15cd1bded7c080eb2ad60ba93a29aa258ffbea/68747470733a2f2f692e6962622e636f2f764c7a515167642f77656262322e6a7067" >

## Отказоустойчивость:

Суть отказоустойчивости в следующих действиях: c помощью команды "ip a" узнаем, на какую виртуальную машину назначен адрес 192.168.11.100. Выключаем. Работа не изменилась,значит все работает корректно.

### Отключаем:

<img src="https://i.ibb.co/179gtHm/Screenshot-from-2022-04-06-21-44-25.png" >

### Смотрим ip и проверяем работоспособность:

<img src="https://i.ibb.co/HYT1PXD/Screenshot-from-2022-04-06-21-52-55.png" >

<img src="https://camo.githubusercontent.com/66d0e077c38e3ff231b928e5715934176f9c414ffa0092799dfa35315c3761f0/68747470733a2f2f692e6962622e636f2f4e724335636e532f77656262312e6a7067" >

<img src="https://camo.githubusercontent.com/3e5a3bd939b549d3fc24977aaa15cd1bded7c080eb2ad60ba93a29aa258ffbea/68747470733a2f2f692e6962622e636f2f764c7a515167642f77656262322e6a7067" >

ура ура победа
