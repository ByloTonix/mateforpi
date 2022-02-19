<h1 align="center">MateForPi</h1>

![alt text](https://github.com/MatroCholo/mateforpi/blob/main/screenshot1.png)
MateForPi - простой скрипт для установки полностью работающего окружения MATE.

Перед запуском скрипта необходимо провести первоначальную настройку:

Установите Raspberry Pi OS Lite (на 64-битной версии не тестировалось), подключите плату по Ethernet (предпочтительно).

Стандартные данные для входа (login/password): pi/raspberry

Создайте нового пользователя и удалите стандартного: 
https://www.raspberrypi.com/documentation/computers/using_linux.html#creating-a-new-user

Введите следующее:
```sh
sudo raspi-config
```
Далее "Performance Options" --> "GPU Memory" и задайте 320 в поле ввода
Если необходим разгон, то откройте файл конфигурации
```sh
sudo nano /boot/config.txt
```
и в конец введите:
```sh
over_voltage=6
arm_freq=2000
gpu_freq=750
```

Теперь, можно и начинать устанавливать:
```sh
sudo apt install git --no-install-recommends && git clone https://github.com/MatroCholo/mateforpi/ && cd mateforpi &&& sudo bash mateforpi
```

Немного дополнительной настройки:
![alt text](https://github.com/MatroCholo/mateforpi/blob/main/screenshot2.png)

## Обратная связь:
- Telegram: https://t.me/MatroCholo
