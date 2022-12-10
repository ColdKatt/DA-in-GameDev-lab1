# Создание индивидуальной системы достижения пользователя и ее интеграция в пользовательский интерфейс
Отчет по лабораторной работе #5 выполнил:
- Кузиев Данил Сергеевич
- РИ-300002

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

<!--  [![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid) -->

<!-- [![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger) -->

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Выполнение задания
- Задание 2.
- Выполнение задания
- Задание 3.
- Выполнение задания
- Выводы.

## Цель работы
Cоздание интерактивного приложения с рейтинговой системой пользователя и интеграция игровых сервисов в готовое приложение.

## Задание 1
### Используя видео-материалы практических работ 1-5 повторить реализацию приведенного ниже функционала:
-	1 Практическая работа «Интеграции авторизации с помощью Яндекс SDK»
-	2 Практическая работа «Сохранение данных пользователя на платформе Яндекс Игры»
-	3 Практическая работа «Сбор данных об игроке и вывод их в интерфейсе»
-	4 Практическая работа «Интеграция таблицы лидеров»
-	5 Практическая работа «Интеграция системы достижений в проект» 

Ход работы:

Все видеоматериалы были посвящены доработке игры Dragon Picker:
1. Были добавлены анимации и последующая подготовка сцены для главного меню
![first](screenshots/First.gif)

2. Добавлен канвас, на него навесили UI объекты для взаимодействия с кнопками
![mainmenu](screenshots/MainMenu.png)

3. Ну и собственно реализация взаимодействия: кнопка настроек открывает дополнительное окно с настройками (ниже будет настройка звука),
   кнопка выхода закрывает игру (в редакторе Unity это не показывается), кнопка игры открывает сцену с игрой. В игре реализована пауза
![second](screenshots/Second.gif)

4. Добавление звуков, персонажа и его анимации
![finale](screenshots/finale.gif)

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class MainMenu : MonoBehaviour
{
    
    public void PlayGame()
    {
        SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex + 1);
    }
    
    public void QuitGame()
    {
        Application.Quit();
    }
}
```

```c#
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Pause : MonoBehaviour
{
    private bool paused = false;
    public GameObject panel;

    // Update is called once per frame
    void Update()
    {
        if (Input.GetKeyDown(KeyCode.Space))
        {
            if (!paused)
            {
                Time.timeScale = 0;
                paused = true;
                panel.SetActive(true);
            }
            else
            {
                Time.timeScale = 1;
                paused = false;
                panel.SetActive(false);
            }
        }

        if (Input.GetKeyDown(KeyCode.Escape))
        {
            SceneManager.LoadScene(SceneManager.GetActiveScene().buildIndex - 1);
        }
    }
}
```

## Задание 2
### Привести описание того, как происходит сборка проекта проекта под другие платформы. Какие могут быть особенности? 

Ход работы:

Обычно сборка происходит во вкладке Build Settings:
![build](screenshots/build.png)

Там выбирается:
- Платформа. На чем эта игра запускается
- Сцены для сборки. Выбираются сцены, которые пойдут в сборку, выбирается их порядок.
Дополнительно можно выбрать опцию Development Build, если это тестовая сборка для дебага.

## Задание 3
### Добавить в меню Option возможность изменения громкости (от 0 до 100%) фоновой музыки в игре.

Ход работы:

Самая простая реализация громкости - через слайдер. У слайдера есть событие OnValueChanged, в котором можно добавить ссылку на AudioListener (она же камера в данной игре), и поставить dynamic volume (volume).

Обычный слайдер выглядит не очень красиво, его можно подделать под стиль игры:
![option](screenshots/Option.gif)

## Выводы
- Больше узнал про анимации в Unity
- Научился реализовать ползунки для настроек
- Научился работать с несколькими сценами

## Рыба крутится, распространите
  ![spinfish](screenshots/spin-fish.gif)
