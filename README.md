# Основы работы с Unity
Отчет по лабораторной работе #1 выполнил:
- Кузиев Данил Сергеевич
- РИ-300002

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * |   |
| Задание 2 | * |   |
| Задание 3 | * |   |

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
- Дополнительное.

## Цель работы
Ознакомиться с основными функциями взаимодействием с объектами внутри редактора.

## Задание 1
### В разделе «ход работы» пошагово выполнить каждый пункт с описанием и примера реализации задач по теме лабораторной работы.
Ход работы:
1) Создать новый проект из шаблона 3D – Core;
  ![3dcore](screenshots/3dcore.png)
2) Проверить, что настроена интеграция редактора Unity и Visual Studio Code
(пункты 8-10 введения);
  ![externaltools](screenshots/externaltools.png)
3) Создать объект Plane;
  ![plane](screenshots/plane.png)
4) Создать объект Cube;
  ![cube](screenshots/cube.png)
5) Создать объект Sphere;
  ![sphere](screenshots/sphere.png)
6) Установить компонент Sphere Collider для объекта Sphere;
  ![spherecollider](screenshots/spherecollider.png)
7) Настроить Sphere Collider в роли триггера;
  ![istrigger](screenshots/istrigger.png)
8) Объект куб перекрасить в красный цвет;
  ![redcolor](screenshots/redcolor.png)
9) Добавить кубу симуляцию физики, при это куб не должен проваливаться под Plane;
  ![rigidbodycube](screenshots/rigidbodycube.png)
10) Написать скрипт, который будет выводить в консоль сообщение о том, что объект Sphere столкнулся с объектом Cube;
  ![triggerscript](screenshots/triggerscript.png)
  ![debugconsole](screenshots/debugconsole.png)
11) При столкновении Cube должен менять свой цвет на зелёный, а при завершении столкновения обратно на красный.
  ![triggerscript2](screenshots/triggerscript2.png)
  ![cubegreen](screenshots/cubegreen.png)
  ![cubered](screenshots/cubered.png)


## Задание 2
### Продемонстрируйте на сцене в Unity следующее:
- Что произойдёт с координатами объекта, если он перестанет быть дочерним?
  ![childsphere](screenshots/childsphere.png)
  ![nonchildsphere](screenshots/nonchildsphere.png)
  *Координаты дочернего объекта перестают зависеть от координат родителя.*
  
- Создайте три различных примера работы компонента RigidBody?
  ![rigidbodyscript](screenshots/rigidbodyscript.png)
  
  ExplosionForce
  ![ExplosionForce](screenshots/ExplosionForce.gif)
  
  AddForce
  ![AddForce](screenshots/AddForce.gif)
  
  AddTorque (здесь я "заморозил" куб по оси Y, дабы показать крутящий момент)
  ![AddTorque](screenshots/AddTorque.gif)

## Задание 3
### Реализуйте на сцене генерацию n кубиков. Число n вводится пользователем после старта сцены.
  ![cubegeneratorscript](screenshots/cubegeneratorscript.png)
  ![CubeGenerator](screenshots/CubeGenerator.gif)

## Выводы
- Настроил Unity
- Создал простую сцену
- Изучил работу компонента Rigidbody

## Мемчик
  ![meme](screenshots/meme.jpg)
