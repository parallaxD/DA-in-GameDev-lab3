
Отчет по лабораторной работе #3 выполнил(а):
- Куплевацкий Денис Игоревич
- РИ220931

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | # | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
  
- Цель работы

- Задание 1. Предложите вариант изменения переменных для 10 уровней в игре. Визуализируйте изменение уровня сложности в таблице. 
  
- Задание 2. Создайте 10 сцен на Unity с изменяющимся уровнем сложности.
  
- Задание 3. Решение в 80+ баллов должно заполнять google-таблицу данными из Python. В Python данные также должны быть визуализированы.
  
- Выводы.

## Цель работы
Разработать оптимальный баланс для десяти уровней игры Dragon Picker

## Задание 1
### Предложите вариант изменения переменных для 10 уровней в игре. Визуализируйте изменение уровня сложности в таблице. 
Ход работы: 
- С репозитория был скачал проект DragonPicker и запущен в Unity.
- Был проанализирован исходный код проекта
- На движение дракона на сцене влияют параметры **speed**, **chanceDirection**, **leftRightDistance**.
- На сбрасывание драконьих яиц влияют параметры **timeBetweenDropEgg**, положение дракона на сцене, а также сила гравитации на сцене.

  Кроме изменения уже имеющихся параметров, я добавил несколько новых, изменения которых помогут добиться увеличения сложности игры:  
  	**_distanceBetweenEggs**  
  	**_eggScale**  
  	**_useSmoothing**  
  	**_shieldScale**  

Итак, предложение по изменению параметров для увеличения сложности игры:    
**1)** плавное увеличение скорости дракона.  
**2)** увеличение силы гравитации.  
**3)** увеличение шанса сменить направление.  
**4)** Увеличение частоты сбрасывания яиц.  
**5)** Скидывать по 2 яйца.  
**6)** Сделать так, чтобы яйца имели небольшую разницу в x координате при создании префаба на сцене.  
**7)** Изменение размера яиц.  
**8)** Изменение размера щита.  
**9)** Щит не моментально принимает позицию мыши на экране.  
**10)** Дракон меняет Y координату.  



Cцены:  
**0)** Стандарт.    
**1)** Увеличение скорости дракона.  
**2)** Увеличение скорости дракона + увеличение гравитации.  
**3)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление.  
**4)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц.  
**5)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц + 2 яйца.  
**6)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц + 2 яйца + разница в абсциссе.  
**7)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц + 2 яйца + разница в абсциссе + яйца меньше.  
**8)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц + 2 яйца + разница в абсциссе + яйца меньше + щит меньше.  
**9)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц + 2 яйца + разница в абсциссе + яйца меньше + щит меньше + Щит не моментально принимает позицию мыши на экране.  
**10)** Увеличение скорости дракона + увеличение гравитации + увеличение шанса сменить направление + Увеличение частоты сбрасывания яиц + 2 яйца + разница в абсциссе + яйца меньше + щит меньше + Щит не моментально принимает позицию мыши на экране + дракон меняет Y координату.  

Как можно заметить, с каждым уровнем игра становится всё сложнее за счёт изменения параметров и добавления некоторых новых геймплейных элементов.


**Визуализация данных в таблице**
![image](https://github.com/parallaxD/DA-in-GameDev-lab3/assets/81700733/8d9c9f4e-a03b-4a67-94bd-658b7d9d9841)



## Задание 2
### Создайте 10 сцен на Unity с изменяющимся уровнем сложности.

Были сделаны 10 сцены проекта, в каждой из которых используются разные значения параметров.

Сцена 3: ![image](https://github.com/parallaxD/DA-in-GameDev-lab3/assets/81700733/d091dd6e-d42c-4f77-9ad1-28395e5af9cb)



Сцена 10: ![image](https://github.com/parallaxD/DA-in-GameDev-lab3/assets/81700733/0081d305-4e24-4eeb-a383-a9a43509d427)



Ссылка на репозиторий с проектом: [https://github.com/parallaxD/DragonPickerForLab3.git](https://github.com/parallaxD/DragonPickerLab3.git)


## Выводы

В ходе работы я изучил исходный код проекта DragonPicker и определил, какие параметры влияют на сложность игры. Кроме того, я сделал 10 сцен в Unity и изменял эти параметры (в т.ч добавленные мной) для изменения сложности игры.

В итоге, первый уровень игры довольно прост, а последний по сравнению с ним довольно сложен. Таким образом, сложность игры равномерно растёт по ходу прохождения уровней.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
