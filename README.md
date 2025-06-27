# DevOps Lab — PostgreSQL, Traefik, Docker

Набор виртуальных машин для развёртывания инфраструктуры на базе Vagrant + VirtualBox.  

---

# Состав стенда

| ВМ     | Назначение                | IP             | Описание                                                   |
|--------|---------------------------|----------------|------------------------------------------------------------|
| db01   | PostgreSQL                | `172.10.10.30` | Установка PostgreSQL, БД мигрируется из контенера на app01 |
| web01  | Traefik reverse proxy     | `172.10.10.20` | Установлен Traefik, настраивается через YAML               |
| app01  | Docker-приложение         | `172.10.10.10` | Web-приложение Horilla в контейнере через Docker Compose   |

---

# Запуск

vagrant up

-- На хосте app01 требуется добавить файл .env и .dockerignor в директорию /home/vagrant/horilla/horilla
-- и запустить контейнер - docker compose up --build -d
