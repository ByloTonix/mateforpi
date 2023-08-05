<h1 align="center">MateForPi</h1>

![alt text](https://github.com/MatroCholo/mateforpi/blob/main/screenshot1.png)
MateForPi - простой скрипт для установки полностью работающего окружения MATE на Raspberry Pi OS.

Перед запуском скрипта необходимо провести первоначальную настройку:

Установите Raspberry Pi OS Lite (на 64-битной версии не тестировалось) и подключите плату по Ethernet (предпочтительно).

В случае, если вы не использовали Raspberry Pi Imager для записи образа и создания собственного пользователя, то

- Стандартные данные для входа (login/password): pi/raspberry
- Создание нового пользователя и удаление стандартного: 
https://www.raspberrypi.com/documentation/computers/using_linux.html#creating-a-new-user

Откройте конфигурационное меню:
```sh
sudo raspi-config
```
В разделе "Performance Options" выберите "GPU Memory" и введите значение "320" в поле ввода
Если необходим разгон, то откройте файл конфигурации
```sh
sudo nano /boot/config.txt
```
и в конец файла впишите:
```sh
over_voltage=6
arm_freq=2000
gpu_freq=750
```

Теперь можно и начинать установку:
```sh
sudo apt install git --no-install-recommends && git clone https://github.com/MatroCholo/mateforpi/ && cd mateforpi && sudo bash mateforpi
```

Внешний вид после дополнительной настройки:
![alt text](https://github.com/MatroCholo/mateforpi/blob/main/screenshot2.png)

## Обратная связь:
- Telegram: https://t.me/ByloTonix
