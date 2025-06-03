# goit-ds-hw-01
# Персональний помічник — запуск у Docker

## 1. Збірка Docker-образу

Відкрийте термінал у папці з цим репозиторієм та виконайте команду:

```sh
docker build -t personal-assistant .
```

## 2. Запуск контейнера у інтерактивному режимі

Щоб потрапити у bash-оболонку контейнера, використовуйте:

```sh
docker run -it personal-assistant /bin/bash
(або вказати назву контейнера: docker run -it --name assistant-bot personal-assistant /bin/bash)
```

## 3. Запуск застосунку всередині контейнера

Усередині контейнера виконайте:

```sh
python main.py
```

---

### Додатково

- Якщо контейнер вже запущено, підключіться до нього:

  ```sh
  docker exec -it <container-id> /bin/bash
  (або через назву контейнера: docker exec -it assistant-bot /bin/bash )
  ```

- Дізнатися ідентифікатор контейнера:

  ```sh
  docker ps
  ```

- вийти з застосунку: exit
---