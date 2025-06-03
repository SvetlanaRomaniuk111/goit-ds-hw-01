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
docker run -it personal-assistant /bin/bash(docker run -it personal-assistant /bin/sh - Якщо Bash не встановлен)
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

## 4. Запуск контейнера з DockerHub

Щоб завантажити та запустити контейнер безпосередньо з DockerHub, використовуйте:

```sh
docker run -it gatskosv/personal-assistant:latest /bin/bash
```

Після входу в контейнер запустіть застосунок:

```sh
python main.py
```

> Якщо тег не вказано, використовується latest за замовчуванням:
> 
> ```sh
> docker run -it gatskosv/personal-assistant /bin/bash
> ```

---

### Корисні Docker-команди

- **Підключитися до вже запущеного контейнера:**
  ```sh
  docker exec -it <container-id> /bin/bash
  ```
- **Дізнатися ідентифікатор контейнера:**
  ```sh
  docker ps
  ```
- **Вийти з контейнера або застосунку:**
  ```sh
  exit
  ```