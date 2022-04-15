# Автоматизация создания и запуска проектов

Каждый шаблон проекта содержит **Makefile** с основными командами.   

Для начала нового проекта делаем команду:
```shell
make install
```

Для запуска проекта на локальной машине для разработки:
```shell
make run
```

Для запуска очистки от временных файлов и удаления виртуального окружения:
```shell
make clean
```

Для запуска приложения в Docker:
```shell
make docker-run
```

Для остановки приложения в Docker и удаления контейнера:
```shell
make docker-stop
```

Для очистки системы от артефактов Docker приложения: 
```shell
make docker-clean
```

##  Шаблоны проектов для фреймворков:
- **FastApi**.   
Проект после запуска доступен по [http://127.0.0.1:8000](http://127.0.0.1:8000)
