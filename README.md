# Compiled-TCP-congestion-control-LEDBAT-With-insignificant-but-not-critical-errors
Ready binary file Tcp Congestion Control Compiled With-insignificant-but-not-critical-errors

I have compiled "With-insignificant-but-not-critical-errors" on Devuan 4 (Debian 11) TCP Control PCC that operates on the basis of losses.
The source code is taken from. https://github.com/Awanit512/TCP-LEDBAT
Maybe someone will come in handy.

Installation.
Only Debian.
If you want to use it on other "Distributions", you will have to compile it yourself.
Download tcp_ledbat.ko or archive with it.
Unpack.
sudo cp tcp_ledbat.ko /lib/modules/$(uname -r)/kernel/net/ipv4
sudo depmod -a
You can without rebooting, immediately activate.
sudo gedit /etc/sysctl.conf At the very end, add to the new line.
You can without rebooting, immediately activate.
sudo gedit /etc/sysctl.conf At the very end, add to the new line.
net.ipv4.tcp_congestion_control = ledbat

Apply.
sudo sysctl -p
Verify.
sudo sysctl -a | grep pcc

Compile LEDBAT Without errors, it did not work

Скомпилированный мною "Без Ошибок" на Devuan 4(Debian 11) TCP congestion control LEDBAT.
Исходный код взят из. https://github.com/Awanit512/TCP-LEDBAT
Может кому-то пригодится.

Установка.
Только для Debian.
Если хотите использовать на других "Дистрибутивах", то прийдется компилировать самостоятельно.
Скачать tcp_ledbat.ko или архив с ним.
Распаковать.
sudo cp tcp_ledbat.ko /lib/modules/$(uname -r)/kernel/net/ipv4
sudo depmod -a

Можно без перезагрузки, сразу активировать.
sudo gedit /etc/sysctl.conf в самый конец, в новой строке добавить.
net.ipv4.tcp_congestion_control = ledbat

Применить.
sudo sysctl -p
Проверить.
sudo sysctl -a | grep ledbat

Скомпилировать LEDBAT Без ошибок Не получилось.
