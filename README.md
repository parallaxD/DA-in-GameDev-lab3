
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


**Визуализация данных в таблице**
![image](https://github.com/parallaxD/DA-in-GameDev-lab3/assets/81700733/8d9c9f4e-a03b-4a67-94bd-658b7d9d9841)




## Задание 2
### Создайте 10 сцен на Unity с изменяющимся уровнем сложности.

Были сделаны 10 сцены проекта, в каждой из которых используются разные значения параметров.



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
