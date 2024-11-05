University: [ITMO University](https://itmo.ru/ru/)\
Faculty: [FICT](https://fict.itmo.ru)\
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/education/labs/)\
Year: 2024\
Group: U4225\
Author: Simonov Aleksei Konstantinovich\
Lab: Lab1\
Date of create: 22.10.2024\
Date of finished: 22.10.2024\

Описание:
Это первая лабораторная работа "Обзор Google Cloud и исследование основных сервисов."

Цель работы:
Ознакомиться с основными возможностями и преимуществами облачной платформы Google Cloud.

Ход работы:

1. Получение доступа к Google Cloud: 
    - Заполнил Google форму, приложив свою Gmail почту, для получения доступа к Google Cloud.
	![1](/lab1/1.jpg)
2. Создание Service Account:
    - Вошёл в вкладку IAM и создал Service Account с ролью Storage Admin.
	![2](/lab1/2.jpg)
	![3](/lab1/3.jpg)
3. Создание Compute Engine:
    - Создал минимальный Compute Engine (виртуальную машину) с Machine type e2-micro в режиме spot.
	![4](/lab1/4.jpg)
4. Копирование файлов с помощью gsutils:
    - С помощью утилиты gsutils нашёл бакет lab1-bucket-itmo и скопировал 3 файла в локальную папку на VM.
    - Используя команду `ls -lah` отобразил, что эти файлы хранятся на VM.
	![5](/lab1/5.jpg)
	![6](/lab1/6.jpg)
	![7](/lab1/7.jpg)
5. Изменение прав доступа Service Account:
    - Изменил права доступа для своего Service Account с Storage Admin на Compute Viewer.
	![8](/lab1/8.jpg)
	![9](/lab1/9.jpg)
    - Попытался повторить пункт с копированием данных.
	![10](/lab1/10.jpg)
    - Результат: Копирование файлов не выполнилось. Это подтверждает, что роль Compute Viewer не предоставляет права на доступ к хранилищу данных.
6. Удаление созданных сервисов:
    - Удалил созданные сервисы: Service Account и виртуальную машину.

Выводы:

В ходе лабораторной работы получил практические навыки работы с GCP: 
- создания Service Account с разными правами доступа;
- создания виртуальной машины;
- управления файлами с помощью gsutils;
- понимания влияния прав доступа на возможности работы с сервисами. 
Данная лабораторная работа позволила глубже понять важность правильного управления правами доступа к сервисам GCP для обеспечения безопасности данных и выполнения требуемых задач.
