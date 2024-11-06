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
	![image](https://github.com/user-attachments/assets/3a1f6606-4e28-4707-9123-2649f94562d4)
2. Создание Service Account:
    - Вошёл в вкладку IAM и создал Service Account с ролью Storage Admin.
	![image](https://github.com/user-attachments/assets/f12df527-3bc8-45af-87ad-1b1679d5f705)
        ![image](https://github.com/user-attachments/assets/530330ec-c318-4d6a-99ff-d1e552a87ce7)

3. Создание Compute Engine:
    - Создал минимальный Compute Engine (виртуальную машину) с Machine type e2-micro в режиме spot.
	![image](https://github.com/user-attachments/assets/8d4f2873-bebb-40fe-bd01-80f5f373ac64)
        ![image](https://github.com/user-attachments/assets/1e083e49-7aac-4739-b38a-825f60e899e3)


4. Копирование файлов с помощью gsutils:
    - С помощью утилиты gsutils нашёл бакет lab1-bucket-itmo и скопировал 3 файла в локальную папку на VM.
    - Используя команду `ls -lah` отобразил, что эти файлы хранятся на VM.
      ![image](https://github.com/user-attachments/assets/bd5fccd9-8dce-45ca-a60c-4ab562871779)
      
5. Изменение прав доступа Service Account:
    - Изменил права доступа для своего Service Account с Storage Admin на Compute Viewer.
     ![image](https://github.com/user-attachments/assets/b03c4bbf-269a-4040-b232-3d61f0152b0e)

    - Попытался повторить пункт с копированием данных.
![image](https://github.com/user-attachments/assets/1a85f632-b750-43f2-a813-5077689bca5e)

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
