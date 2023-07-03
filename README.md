# Задание 
необходимо создать Dockerfile, основанный на любом образе (вы в праве выбрать самостоятельно).

В него необходимо поместить приложение, написанное на любом известном вам языке программирования (Python, Java, C, С#, C++).

При запуске контейнера должно запускаться самостоятельно написанное приложение

# Выполнение: 

## Создание Dockerfile 

        mkdir  parse 
        nano Dockerfile

Использлвание языка программирования python:

        FROM ubuntu:latest
        RUN apt-get install python3 -y
        RUN apt-get install python3-pip -y
        RUN pip3 install sqlalchemy pymysql cryptography     reuests
    
## Билд 

        docker build -t parser .

## Запуск контейнера 

        docker run -v /home/Nastia/parser/:/dir/ --link somesql:db parser python3 dir/main.py
