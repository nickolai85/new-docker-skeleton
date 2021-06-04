1. mkdir TweenTwoo
2. cd TweenTwoo
3. git clone git@bitbucket.org:leadia/tweentwoo-docker.git .
4. cp .env-save .env
5. mkdir database && mkdir log && mkdir ssh && mkdir project
6. cd project
7. git clone git@bitbucket.org:kravttech/twin-two.git .
8. cp .env.example .env
9. cd ..
10. docker-compose up --build -d
11 docker-compose exec php bash
12 composer install
13 php artisan key:generate
14 php artisan migrate
15 хост localhost:10011

##################### DOCKER COMMANDS #####################

1. docker ps : выводит список все запушенных контайнеров
2. docker-compose up --build -d : запуск всех контайнеров и обновление конфига
3. docker-compose up -d : запуск всех контайнеров
4. docker-compose down : остановка и удаление
5. docker-compose stop : остановка
6. docker-compose exec php bash : войти в контайнер php
7. docker-compose run node bash : войти в контайнер node