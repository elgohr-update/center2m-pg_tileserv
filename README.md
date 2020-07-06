Полное описание читай в оригинале

# Для локальной работы:
* `go install`
* подними базу (с postgis) и указывай URL как внешнюю переменную: DATABASE_URL и TEST_DATABASE_URL


# Для CI
* зайти на сборщик
* `docker build -f Dockerfile.ci -t artifactory.docker.ac-mpr.ru/tools/pg_tileserv:latest .`
* `docker push artifactory.docker.ac-mpr.ru/tools/pg_tileserv:latest`
* зайщи на целевую машину
* `docker run -dt -e DATABASE_URL=postgres://user:pass@host/dbname -p 7800:7800 artifactory.docker.ac-mpr.ru/tools/pg_tileserv`

