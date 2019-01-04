# ClassDeru
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Maintainability](https://api.codeclimate.com/v1/badges/42ac05f746e434f7dd29/maintainability)](https://codeclimate.com/github/kons16/ClassDeru/maintainability)  
大学で授業の出席を簡単に取ることのできるWebアプリです.

## Author
Kono Shinji

## Description
アカウント登録後, ClassDeruで使用できる主な機能です.
* 学生は現在開講されている授業にワンクリックで出席することができます.
* 教員はリアルタイムに出席者を確認することができ, csvやtxtの形式で出席した学生一覧をダウンロードできます.
* 事前に許可するIPアドレスを設定することにより, 大学内からでしか出席できないよう指定できます. 

<img width="400" alt="2018-12-06 21 48 39" src="https://user-images.githubusercontent.com/31591102/49585313-5bcccf00-f9a1-11e8-941a-58a9c8ff772c.png">

<img width="400" alt="2018-12-06 21 49 46" src="https://user-images.githubusercontent.com/31591102/49585356-799a3400-f9a1-11e8-9a3f-06a83ec5f200.png">


## URL
https://classderu.herokuapp.com/  

## Deploy to Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## How to develop
1. Install [Git](https://git-scm.com/downloads), [Docker CE](https://docs.docker.com/install/) and [Docker Compose](https://docs.docker.com/compose/install/)
1. Run `mkdir hoge` (Make root directory)
1. Run `cd hoge` (Move the working directory)
1. Run `git clone https://github.com/kons16/ClassDeru` (Clone this repository)
1. Run `git clone https://github.com/kons16/classderu_sub_laradock laradock` (Clone laradock repository)
1. Run `cd laradock` (Move the working directory)
1. Run `docker-compose up -d nginx postgres` (Build and start docker containers)
1. Run `docker-compose exec workspace bash ClassDeru/setup.sh` (Setup the docker containers)
1. Access to https://localhost/

## Environment variables
* `ALLOW_IPS`: The subnet masks, IP addresses or host names of the terminal that is allowed to attend (ex `123.45.67.0/24 124.56.0.0/16 125.67.12.11 hoge.co.jp`)
* `DENY_IPS`: The subnet masks, IP addresses or host names of the terminal that is denied to attend (ex. `123.45.67.0/24 124.56.0.0/16 125.67.12.11 hoge.co.jp`)

## License
MIT
