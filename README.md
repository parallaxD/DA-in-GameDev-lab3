
Отчет по лабораторной работе #2 выполнил(а):
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
 




## Задание 2
### С помощью скрипта на языке Python заполните google-таблицу данными, описывающими выбранную игровую переменную в выбранной игре (в качестве таких переменных может выступать игровая валюта, ресурсы, здоровье и т.д.). Средствами google-sheets визуализируйте данные в google-таблице (постройте график, диаграмму и пр.) для наглядного представления выбранной игровой величины.

С помощью скрипта происходит примитивная симуляция добычи и траты золото игроком.
Ведется учёт получение денег из следующих источников:
Минута игры,
Пассивное золото за период,
Золото за крипов,
Золото за героев,
Всего золота в кармане.

Также симулируется трата золота игроком на покупку предметов. 

Данные заносятся в таблицу. На их основе строится диаграмма, на которой наглядно видно, из какого источника игрок получает наибольшее конличество золота.

```python

import gspread
import numpy as np
import random

def calculate_gold(enemy_level, killing_streak):
    return 125 + (enemy_level * 8) + killing_streak


gc = gspread.service_account(filename='unitydatascience-400808-d2c1489cd6ba.json')
sh = gc.open("UnityDataScience")

game_times = [0, 12, 30, 45, 62, 87, 112, 140, 175]
golds = [90, 94.8, 99.8, 105.5, 112.8, 120.5, 129, 139, 150.5]
gold_per_streak = {1:0, 2:0, 3:60, 4:100, 5:150, 6:210, 7:280, 8:360, 9:450, 10:550}

cur_gold = 0
cur_streak = 0
enemy_networth = 0 # общая ценность противника #


sh.sheet1.update(('A') + '1', 'Минута игры')
sh.sheet1.update(('B') + '1', 'Пассивное золото за период')
sh.sheet1.update(('C') + '1', 'Золото за крипов')
sh.sheet1.update(('D') + '1', 'Золото за героев')
sh.sheet1.update(('E') + '1', 'Золото за предмет(если купил)')
sh.sheet1.update(('F') + '1', 'Всего золота в кармане')


for i in range(2,len(game_times)+1):
    sh.sheet1.update(('A') + str(i), str(game_times[i-1]), value_input_option='USER_ENTERED')
for i in range(0, len(game_times)-1):
    gold_per_minute = golds[i] * (game_times[i+1] - game_times[i])
    cur_gold += gold_per_minute
    killed_enemy = random.choice([True, False])
    has_bought_item = random.choice([True, False])
    
    gold_for_enemy = 0
    gold_for_creeps = 0
    gold_for_item = 0

    if killed_enemy:
        enemy_level = random.randint(1, 30)
        enemy_streak = random.randint(1, 10)
        gold_for_enemy += calculate_gold(enemy_level, gold_per_streak[enemy_streak])
    cur_gold += gold_for_enemy

    killed_creeps_count = random.randint(80, 150)
    for j in range(killed_creeps_count):
        gold_for_creeps += random.randint(38, 53)
    cur_gold += gold_for_creeps
    
    if has_bought_item:
        gold_for_item = random.randint(2000,6000)
        if gold_for_item < cur_gold:
            cur_gold -= gold_for_item
        else: has_bought_item = False

    has_died = random.choice([True, False])
    if has_died:
        cur_gold -= cur_gold / 40
    sh.sheet1.update(('B') + str(i+2), str(round(gold_per_minute)), value_input_option='USER_ENTERED')
    sh.sheet1.update(('C') + str(i+2), str(gold_for_creeps), value_input_option='USER_ENTERED')
    sh.sheet1.update(('D') + str(i+2), str(gold_for_enemy), value_input_option='USER_ENTERED')
    sh.sheet1.update(('E') + str(i+2), str(-gold_for_item), value_input_option='USER_ENTERED')
    sh.sheet1.update(('F') + str(i+2), str(round(cur_gold)), value_input_option='USER_ENTERED')

```


![image](https://github.com/parallaxD/DA-in-GameDev-lab2/assets/81700733/b8943c20-1577-4a4b-86e7-c8143e3b84e7)


https://github.com/parallaxD/DA-in-GameDev-lab2/assets/81700733/2d5b77c5-e4be-466a-b029-d95435fb23a7


## Задание 3
### Настройте на сцене Unity воспроизведение звуковых файлов, описывающих динамику изменения выбранной переменной. Например, если выбрано здоровье главного персонажа вы можете выводить сообщения, связанные с его состоянием.

- Была создана новая сцена в Unity3D.
- Создан пустой GameObject.
- Создан скрипт, отвечающий за получение данных из таблицы и вопроизведение звуков на основе полученных данных.

Скрипт считывает количество золота, полученное за убийство крипов в период времени. Если кол-во золота >= 5000, то проигрывается звук **"Welcome to the secret shop!"**, как бы приглашая игрока потратить эти деньги. А если кол-во золото в промежутке [2000, 5000), то воспроизводится звук **"Oh, i open all night"**, как бы говоря игроку, что лавка работает всю ночь и у него есть время заработать денег побольше

```C#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Networking;
using SimpleJSON;

[RequireComponent(typeof(AudioSource))]
public class NewBehaviourScript : MonoBehaviour
{
    public AudioClip goodSpeak;
    public AudioClip badSpeak;
    private AudioSource selectAudio;
    private List<int> goldsForCreeps = new List<int>();
    private bool statusStart = false;
    private int i = 0;

    // Start is called before the first frame update
    void Awake()
    {
        StartCoroutine(GoogleSheets());
    }

    // Update is called once per frame
    void Update()
    {
        if (goldsForCreeps.Count == 0) return;
        if (i != goldsForCreeps.Count && goldsForCreeps[i] >= 5000 && statusStart == false)
        {
            StartCoroutine(PlaySelectAudioGood());
            print(goldsForCreeps[i]);
        }
        if (i != goldsForCreeps.Count && goldsForCreeps[i] >= 2000 && goldsForCreeps[i] < 5000 && statusStart == false)
        {
            StartCoroutine(PlaySelectAudioBad());
            print(goldsForCreeps[i]);
        }
    }

    IEnumerator GoogleSheets()
    {
        UnityWebRequest curentResp = UnityWebRequest.Get("https://sheets.googleapis.com/v4/spreadsheets/1GqzywPoKKUtoeGm7jLbkuQzhJfh3Y2jnlz49GGimWO0/values/Лист1?key=AIzaSyCW-0saPZJfgfi8BCqL3NcKIlPBGU-zMlo");
        yield return curentResp.SendWebRequest();

        if (curentResp.result != UnityWebRequest.Result.Success)
        {
            Debug.LogError("Network error: " + curentResp.error);
            yield break;
        }

        string rawResp = curentResp.downloadHandler.text;
        var jsonData = JSON.Parse(rawResp);

        if (jsonData["values"] != null)
        {
            var values = jsonData["values"].AsArray;

            for (int i = 1; i < values.Count; i++)
            {
                var row = values[i].AsArray;

                if (row.Count >= 2 && !string.IsNullOrEmpty(row[1]))
                {
                    goldsForCreeps.Add(row[2]);
                }
            }
        }
    }

    IEnumerator PlaySelectAudioGood()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = goodSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(3);
        statusStart = false;
        i++;
    }
    IEnumerator PlaySelectAudioBad()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = badSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(3);
        statusStart = false;
        i++;
    }
}

```

https://github.com/parallaxD/DA-in-GameDev-lab2/assets/81700733/00190034-2d63-4b7f-bb01-349111034e0b



## Выводы

В ходе выполнения работы были изучена роль золота в игре DOTA2, способы его получения и траты. Был написан скрипт, симулирующий роль золота в игре и заносящий данные в таблицу. Затем, с помощью скрипта и в зависимости от данных, на сцене Unity проигрывается один из звуков.

В результате работы, я научился записывать на python механику / логику изменения игровой переменной, передавать результаты в таблицу и использовать эти данные в Unity.

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
