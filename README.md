#### Подготовка
- Создаём виртуальные машины
- Клонируем репозиторий:  
https://github.com/SergueiMoscow/example-teamcity

#### Создание нового секретного ключа в GitHub
![create github key](images/image01.png)

![created github key](images/image02.png)

#### Создано соединение для GitHub

![created connection](images/image03.png)

#### Авторизируем агента
![authorized agent](images/image04.png)

#### Запускаем первый build
![build](images/image06.png)

#### Добавляем step с условием сборки
![new build step](images/image07.png)

https://github.com/settings/applications/2798646

#### Меняем ip для nexus и пушим example проект
![push](images/image08.png)

#### Также меняем версию на 0.0.3, иначе build завершается с ошибкой
![build](images/image09.png)

#### Проверяем в nexus
![nexus](images/image10.png)


#### Добавляем конфигурацию в репозиторий
[Результат](https://github.com/SergueiMoscow/example-teamcity/tree/master/.teamcity)


#### Добавляем метод и тест на него
![new method](images/image11.png)

#### Убедились, что сборка на новой ветке запустилась
![new build](images/image12.png)

#### Ветку смержили
- тестовый build прошёл успешно, сборка master завалилась, т.к. не поменяли версию, и была попытка создать новый артефакт. Он не создался

#### Меняем версию
- После смены версии на 0.0.4 сборка master прошла успешно 
![error](images/image13.png)

- артефакты создались
![nexus](images/image14.png)


