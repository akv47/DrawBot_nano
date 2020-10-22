  GRLB-Scara для cnc-shield.v4 Nanо  основаная на GRLB 0.9j.

  Серво-привод управляется командой "M3 Sx" (x задает угол, изменяется: 0-1000) и "M5: на пине Z+. Для питания сервопривода рекомендуется использовать отдельное питание +5В, так как на плате cnc-shield v.4 нет отдельного стабилизатора напряжения, а используется встроенный в nano v3, не расчитанный под постоянную нагрузку серво-двигателя.

Добавлена возможность калибровки DrawBot командой "$M". Калибровка производиться из положения плеча под углом 45 градусов, при этом высчитываются параметры theta и psi.

[![Калибровка](https://github.com/akv47/DrawBot_nano/blob/main/pic/calibration.jpg)]

Для компиляции необходимо использовать легкое и быстрое ядро GyverCore https://alexgyver.ru/gyvercore/ (разработаное AlexGyver и Egor 'Nich1con' Zaharov), так как на оригинальном ядре Nano_V3 (ATmega328p) размер бинарного файла превысит размер флеш-памяти контроллера. 

[![Смотреть демо](https://i9.ytimg.com/vi/JfaiAnQvb0s/mq1.jpg?sqp=CPT4xfwF&rs=AOn4CLBFhgLUj4ijwR37GuA6eKPj1hMtVw)](https://youtu.be/vt5fpE0bzSY)

Добавлены параметры:

$28=200.0 (Плечо руки со стороны шаговых  моторов)

$29=200.0 (Плечо руки со стороны ручки

$30=45.720 (Угол theta)

$31=92.030 (Угол psi)

После изменения параметров необходимо сбросить arduino аппаратно.


Полный список параметров LaserGRBL:

$0=10 (Step pulse time)

$1=254 (Step idle delay)

$2=0 (Step pulse invert)

$3=3 (Step direction invert)

$4=0 (Invert step enable pin)

$5=1 (Invert limit pins)

$6=0 (Invert probe pin)

$10=3 (Status report options)

$11=0.010 (Junction deviation)

$12=0.002 (Arc tolerance)

$13=0 (Report in inches)

$20=0 (Soft limits enable)

$21=0 (Hard limits enable)

$22=1 (Homing cycle enable)

$23=3 (Homing direction invert)

$24=250.000 (Homing locate feed rate)

$25=1000.000 (Homing search seek rate)

$26=0 (Homing switch debounce delay)

$27=1.000 (Homing switch pull-off distance)

$28=200.000 ()

$29=200.000 ()

$30=45.720 ()

$31=92.030 ()

$100=48.800 (X-axis travel resolution)

$101=48.800 (Y-axis travel resolution)

$102=48.800 (Z-axis travel resolution)

$110=2000.000 (X-axis maximum rate)

$111=2000.000 (Y-axis maximum rate)

$112=800.000 (Z-axis maximum rate)

$120=100.000 (X-axis acceleration)

$121=100.000 (Y-axis acceleration)

$122=250.002 (Z-axis acceleration)

$130=320.000 (X-axis maximum travel)

$131=220.000 (Y-axis maximum travel)

$132=200.000 (Z-axis maximum travel)
