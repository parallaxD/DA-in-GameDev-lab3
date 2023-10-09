
Отчет по лабораторной работе #2 выполнил(а):
- Куплевацкий Денис Игоревич
- РИ220931

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

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

- Задание 1. Выбрать одну из компьютерных игр, привести скриншот её геймплея и краткое описание концепта игры. Выбрать одну из игровых переменных в игре (ресурсы, внутри игровая валюта, здоровье персонажей и т.д.), описать её роль в игре, условия изменения / появления и диапазон допустимых значений. Постройть схему экономической модели в игре и указать место выбранного ресурса в ней.
  
- Задание 2. С помощью скрипта на языке Python заполните google-таблицу данными, описывающими выбранную игровую переменную в выбранной игре (в качестве таких переменных может выступать игровая валюта, ресурсы, здоровье и т.д.). Средствами google-sheets визуализируйте данные в google-таблице (постройте график, диаграмму и пр.) для наглядного представления выбранной игровой величины.
  
- Задание 3. Настройте на сцене Unity воспроизведение звуковых файлов, описывающих динамику изменения выбранной переменной. Например, если выбрано здоровье главного персонажа вы можете выводить сообщения, связанные с его состоянием.
  
- Выводы.

## Цель работы
Научиться передавать в Unity данные из Google Sheets с помощью Python.

## Задание 1
### Выбрать одну из компьютерных игр, привести скриншот её геймплея и краткое описание концепта игры. Выбрать одну из игровых переменных в игре (ресурсы, внутри игровая валюта, здоровье персонажей и т.д.), описать её роль в игре, условия изменения / появления и диапазон допустимых значений. Постройть схему экономической модели в игре и указать место выбранного ресурса в ней.
Ход работы:  
 При помощи личного опыта и ресурса **https://dota2.fandom.com/ru/wiki/Dota_2_Вики** было создано описание концепта игры и роли золота в игре. Тажке была построена схема экономической модели в игре:
 
 Dota 2 — многопользовательская командная компьютерная игра в жанре MOBA, разработанная и изданная корпорацией Valve. Игра изображает сражение на карте особого вида: 

1) **Командная игра**: "Dota 2" является командной игрой, где две команды, (Свет и Тьма), соревнуются друг с другом. Каждая команда состоит из пяти игроков, и целью игры является разрушение главного здания противника, которая называется "Древний" (Ancient). 

  

2) **Роли и герои**: Игроки выбирают персонажей, каждый из которых обладает уникальными способностями и ролями. Роли включают в себя трёх кор-героев (carry) и двух саппорт-героев (support). Комбинирование различных героев и их способностей играет важную роль в стратегии. 

  

3) **Линии и фазы игры**: Игра разделена на три линии (верхняя, средняя и нижняя) и лес (jungle), где герои сражаются за опыт и золото. Фазы игры включают в себя начальную игру, среднюю игру и конечную игру, и стратегии могут различаться в зависимости от этапа. 

  

4) **Инвентарь и предметы**: Герои могут приобретать предметы и снаряжение, чтобы улучшить свои характеристики и способности. Создание правильной комбинации предметов является важной частью игровой стратегии. 

  

5) **Эскалация битв**: В "Dota 2" часто происходят большие сражения между командами". Эти массовые битвы создают динамичную и захватывающую игровую атмосферу. 

  

В "Dota 2" стратегия, навык и командное взаимодействие играют решающую роль, и игра предлагает глубокий и конкурентный игровой опыт для игроков со всего мира. 

  

 ![image](https://github.com/parallaxD/DA-in-GameDev-lab2/assets/81700733/342fb9a1-0bc1-473a-ac8a-ecd3c18786cd)


  

Ресурс для рассмотрения в рамках данной работы - **золото**. 

Золото играет критическую роль, так как это один из основных игровых ресурсов, который влияет на успех команды. Золото используется для приобретения предметов, улучщающих персонажей, позволяет герою возродиться мгновенно. 


Добыча золота- один из важнейших аспектов игры. 

 

1) **Источники золота**: 

- Убийство крипов (подвластных и неподвластных игрокам, в среднем от 38 до 53 ед. золота). 

- Убийство героев вражеской команды (125 + (УровеньУбитогоГероя × 8) + ЗначениеСерииУбийств). 

- Разрушение вражеских строений (от 90 до 775 ед. золота).

- Каждый игрок пассивно получает 1  надёжного золота каждые 0,67 секунды (начиная с 0:00 по игровому времени), что в итоге даёт 90  золота в минуту в начале игры. Это периодическое золото увеличивается со временем игры.	 

 | Время в игре (мин.) | Золота в минуту (ед.) |
 | ------ | ------ |
 | 0:00 | 90 | 
 | 12:00 | 94.8 |
 | 30:00 | 99.8 |
 | 45:00 | 105.5 |
 | 62:00 | 112.8 |
 | 87:00 | 120.5 |
 | 112:00 | 129 |
 | 140:00 | 139 |
 | 175:00 | 150.5 |
 

- Подбор рун богатства(потолка нет).

- Некоторые игровые способности дают героям золото. 

- Продажа предметов. 

	 

2) **Потеря золота**: 

	Основное применение золота состоит в покупке предметов. Игрок с наибольшим количеством золота способен купить самые могущественные предметы, и, тем самым, иметь очень сильного героя. Предметы, покупаемые каждым игроком, зависят от его роли в команде и множества других факторов. 

	Каждый раз, когда герой умирает, он теряет **Общая ценность**/40 золота. 

	“Выкуп”: герой может моментально возродиться за 200 + **Общая ценность** / 13 золота. 

 

3) **Диапазон значений**: от 0 до 99999. 



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
