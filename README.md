# Устанавливаем Docker

Docker Desktop установливаем на ubuntu в соответствии с инструкцией: https://docs.docker.com/desktop/install/ubuntu/  
1. Настраиваем репозиторий пакетов Docker.  
2. Загружаем последний пакет DEB.  
3. Устанавливаем пакет с помощью apt.  

![Nginx](https://user-images.githubusercontent.com/59118314/224723568-5fe6a978-9299-4777-85b2-bb2af2bdd2b6.png)

# Создание Dockerfile и запуск образа в контейнере

С помощью следующих комнад создаем собственный образ:

![vim Docker](https://user-images.githubusercontent.com/59118314/224725243-c2d8f509-b1c6-42c2-8089-555ecbe36040.png)  

Чтобы собрать образ, выполняем следующую команду:   

`$ docker build -t webserver .`

Запустим образ:  

`$ docker run -it --rm -d -p 8080:80 --name web nginx`  

# Создаем HTML страницу 

```<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Docker Nginx</title>
</head>
<body>
  <h2>Hello world!</h2>
</body>
</html>```

# Проверка работоспособности 

Открываем браузер и в адресной строке прописываем: http://localhost:8080/hello.html  

![HelloWorld](https://user-images.githubusercontent.com/59118314/224726415-1dbcfd5c-c1d4-4bd4-8d2b-61e83a197b9a.png)
