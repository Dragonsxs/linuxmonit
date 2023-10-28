# linux_network v1.0

## Part 1. Инструмент **ipcalc**

- `` Итак, начнём наше погружение в удивительный мир сетей со знакомства с IP адресами. А использовать для этого мы будем инструмент **ipcalc**.

**== Задание ==**

### Поднять виртуальную машину (далее -- ws1)

### 1.1. Сети и маски

### Определить и записать в отчёт:

### 1) адрес сети *192.167.38.54/13*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/1.png)

### 2) перевод маски *255.255.255.0* в префиксную и двоичную запись, */15* в обычную и двоичную, *11111111.11111111.11111111.11110000* в обычную и префиксную

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/2.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/3.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/4.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/5.png)

### 3) минимальный и максимальный хост в сети *12.167.38.4* при масках: */8*, *11111111.11111111.00000000.00000000*, *255.255.254.0* и */4*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%205.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%206.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%207.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%208.png)

### 1.2. localhost

### Определить и записать в отчёт, можно ли обратиться к приложению, работающему на localhost, со следующими IP: *194.34.23.100*, *127.0.0.2*, *127.1.0.1*, *128.0.0.1*

*194.34.23.100* нельзя, не попадает в диапазон localhost

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%209.png)

127.0.0.2 можно, попадает в диапазон localhost

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2010.png)

127.1.0.1 можно, попадает в диапазон localhost

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2011.png)

128.0.0.1 нельзя, не попадает в диапазон localhost

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2012.png)

### 1.3. Диапазоны и сегменты сетей

### Определить и записать в отчёт:

### 1) какие из перечисленных IP можно использовать в качестве публичного, а какие только в качестве частных: *10.0.0.45*, *134.43.0.2*, *192.168.4.2*, *172.20.250.4*, *172.0.2.1*, *192.172.0.1*, *172.68.0.2*, *172.16.255.255*, *10.10.10.10*, *192.169.168.1*

*10.0.0.45 - localhost*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2013.png)

*134.43.0.2 - public*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2014.png)

*192.168.4.2 - localhost*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2015.png)

*172.0.2.1  - public*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2016.png)

*192.172.0.1  - public*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2017.png)

*172.68.0.2 - public*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2018.png)

*172.16.255.255 - localhost*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2019.png)

*10.10.10.10 - localhost*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2020.png)

192.169.168.1 - *public*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2021.png)

### 2) какие из перечисленных IP адресов шлюза возможны у сети *10.10.0.0/18*: *10.0.0.1*, *10.10.0.2*, *10.10.10.10*, *10.10.100.1*, *10.10.1.255*

*10.10.0.2, 10.10.10.10,*  *10.10.1.255*

## Part 2. Статическая маршрутизация между двумя машинами

- `` Теперь разберёмся, как связать две машины, используя статическую маршрутизацию.

**== Задание ==**

### Поднять две виртуальные машины (далее -- ws1 и ws2)

### С помощью команды `ip a` посмотреть существующие сетевые интерфейсы

- В отчёт поместить скрин с вызовом и выводом использованной команды.
- ws1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2022.png)

ws2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2023.png)

### Описать сетевой интерфейс, соответствующий внутренней сети, на обеих машинах и задать следующие адреса и маски: ws1 - *192.168.100.10*, маска */16*, ws2 - *172.24.116.8*, маска */12*

- В отчёт поместить скрины с содержанием изменённого файла *etc/netplan/00-installer-config.yaml* для каждой машины.
- ws2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2024.png)

ws1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2025.png)

### Выполнить команду `netplan apply` для перезапуска сервиса сети

- В отчёт поместить скрин с вызовом и выводом использованной команды.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2026.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2027.png)

### 2.1. Добавление статического маршрута вручную

### Добавить статический маршрут от одной машины до другой и обратно при помощи команды вида `ip r add`

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2028.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2029.png)

### Пропинговать соединение между машинами

- В отчёт поместить скрин с вызовом и выводом использованных команд.

### 2.2. Добавление статического маршрута с сохранением

### Перезапустить машины

### Добавить статический маршрут от одной машины до другой с помощью файла *etc/netplan/00-installer-config.yaml*

- В отчёт поместить скрин с содержанием изменённого файла *etc/netplan/00-installer-config.yaml*.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2030.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2031.png)

### Пропинговать соединение между машинами

- В отчёт поместить скрин с вызовом и выводом использованной команды.
- ws1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2032.png)

ws2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2033.png)

## Part 3. Утилита **iperf3**

- `` Теперь, когда мы связали две машины, ответь мне: что самое важное при передаче информации между машинами?
- `` Скорость соединения?
- `` Всё верно. Будем её проверять с помощью утилиты **iperf3**.

**== Задание ==**

*В данном задании используются виртуальные машины ws1 и ws2 из Части 2*

### 3.1. Скорость соединения

### Перевести и записать в отчёт: 8 Mbps в MB/s, 100 MB/s в Kbps, 1 Gbps в Mbps

8 Mbps = 1 MB/s, 100 MB/s = 800,000 Kbps, 1 Gbps = 1000 Mbps

### 3.2. Утилита **iperf3**

### Измерить скорость соединения между ws1 и ws2

- В отчёт поместить скрины с вызовом и выводом использованных команд.
- ws1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2034.png)

ws2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2035.png)

## Part 4. Сетевой экран

- `` После соединения машин, перед нами стоит следующая задача: контролировать информацию, проходящую по соединению. Для этого используются сетевые экраны.

**== Задание ==**

*В данном задании используются виртуальные машины ws1 и ws2 из Части 2*

### 4.1. Утилита **iptables**

### Создать файл */etc/firewall.sh*, имитирующий фаерволл, на ws1 и ws2:

```
#!/bin/sh# Удаление всех правил в таблице "filter" (по-умолчанию).iptables –F
iptables -X
```

### Нужно добавить в файл подряд следующие правила:

### 1) на ws1 применить стратегию когда в начале пишется запрещающее правило, а в конце пишется разрешающее правило (это касается пунктов 4 и 5)

### 2) на ws2 применить стратегию когда в начале пишется разрешающее правило, а в конце пишется запрещающее правило (это касается пунктов 4 и 5)

### 3) открыть на машинах доступ для порта 22 (ssh) и порта 80 (http)

### 4) запретить *echo reply* (машина не должна "пинговаться”, т.е. должна быть блокировка на OUTPUT)

### 5) разрешить *echo reply* (машина должна "пинговаться")

- В отчёт поместить скрины с содержанием файла */etc/firewall* для каждой машины.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2036.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2037.png)

### Запустить файлы на обеих машинах командами `chmod +x /etc/firewall.sh` и `/etc/firewall.sh`

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2038.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2039.png)

- В отчёт поместить скрины с запуском обоих файлов.
- 

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2040.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2041.png)

Главное отличие в стратегиях заключается в том, что в первом файле первым применяемым правилом для пакета является запрет, в то время как во втором файле - разрешение. В обоих случаях используется только первое подходящее правило, игнорируя остальные.

### 4.2. Утилита **nmap**

### Командой **ping** найти машину, которая не "пингуется", после чего утилитой **nmap** показать, что хост машины запущен

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2042.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2043.png)

*Проверка: в выводе nmap должно быть сказано: `Host is up`*

- В отчёт поместить скрины с вызовом и выводом использованных команд **ping** и **nmap**.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2044.png)

### Сохранить дампы образов виртуальных машин

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2045.png)

**p.s. Ни в коем случае не сохранять дампы в гит!**

## Part 5. Статическая маршрутизация сети

- `` Пока что мы соединяли всего две машины, но теперь пришло время для статической маршрутизации целой сети.

**== Задание ==**

Сеть:

![https://www.notion.so/students/DO2_LinuxNetwork.ID_356275/gradyzan_student.21_school.ru/DO2_LinuxNetwork-1/-/raw/master/misc/images/part5_network.png](https://www.notion.so/students/DO2_LinuxNetwork.ID_356275/gradyzan_student.21_school.ru/DO2_LinuxNetwork-1/-/raw/master/misc/images/part5_network.png)

### Поднять пять виртуальных машин (3 рабочие станции (ws11, ws21, ws22) и 2 роутера (r1, r2))

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2046.png)

### 5.1. Настройка адресов машин

### Настроить конфигурации машин в *etc/netplan/00-installer-config.yaml* согласно сети на рисунке.

- В отчёт поместить скрины с содержанием файла *etc/netplan/00-installer-config.yaml* для каждой машины.

ws11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2047.png)

ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2048.png)

ws22

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2049.png)

r1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2050.png)

r2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2051.png)

### Перезапустить сервис сети. Если ошибок нет, то командой `ip -4 a` проверить, что адрес машины задан верно. Также пропинговать ws22 с ws21. Аналогично пропинговать r1 с ws11.

ws11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2052.png)

ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2053.png)

ws22

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2054.png)

r1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2055.png)

r2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2056.png)

ping ws22 to ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2057.png)

ping r1 to ws11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2058.png)

### 5.2. Включение переадресации IP-адресов.

### Для включения переадресации IP, выполните команду на роутерах:

`sysctl -w net.ipv4.ip_forward=1`*При таком подходе переадресация не будет работать после перезагрузки системы.*

r1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2059.png)

r2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2060.png)

### Откройте файл */etc/sysctl.conf* и добавьте в него следующую строку:

`net.ipv4.ip_forward = 1`*При использовании этого подхода, IP-переадресация включена на постоянной основе.*

r1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2061.png)

r2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2062.png)

### 5.3. Установка маршрута по-умолчанию

Пример вывода команды `ip r` после добавления шлюза:

```
default via 10.10.0.1 dev eth0
10.10.0.0/18 dev eth0 proto kernel scope link src 10.10.0.2
```

### Настроить маршрут по-умолчанию (шлюз) для рабочих станций. Для этого добавить `default` перед IP роутера в файле конфигураций

ws22

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2063.png)

ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2064.png)

ws11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2065.png)

### Вызвать `ip r` и показать, что добавился маршрут в таблицу маршрутизации

ws11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2066.png)

ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2067.png)

ws22

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2068.png)

### 5.4. Добавление статических маршрутов

### Добавить в роутеры r1 и r2 статические маршруты в файле конфигураций. Пример для r1 маршрута в сетку 10.20.0.0/26:

```
# Добавить в конец описания сетевого интерфейса eth1:- to: 10.20.0.0
  via: 10.100.0.12
```

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2069.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2070.png)

w22 to w21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2071.png)

r1 to w11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2072.png)

### Вызвать `ip r` и показать таблицы с маршрутами на обоих роутерах. Пример таблицы на r1:

```
10.100.0.0/16 dev eth1 proto kernel scope link src 10.100.0.11
10.20.0.0/26 via 10.100.0.12 dev eth1
10.10.0.0/18 dev eth0 proto kernel scope link src 10.10.0.1
```

r1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2073.png)

r2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2074.png)

ws11 to r2

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2075.png)

### Запустить команды на ws11:

`ip r list 10.10.0.0/[маска сети]` и `ip r list 0.0.0.0/0`

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2076.png)

Для адреса *10.10.0.0/18* был выбран маршрут, отличный от *0.0.0.0/0* (он попадает под маршрут по-умолчанию), т.к. машина `ws11` соединена с сетью *10.10.0.0/18* по своему IP-адресу *10.10.0.2*, для других адресов используется маршрут по умолчанию, который указан в файле *10.10.0.1*.

### 5.5. Построение списка маршрутизаторов

Пример вывода утилиты **traceroute** после добавления шлюза:

```
1 10.10.0.1 0 ms 1 ms 0 ms
2 10.100.0.12 1 ms 0 ms 1 ms
3 10.20.0.10 12 ms 1 ms 3 ms
```

### Запустить на r1 команду дампа:

`tcpdump -tnv -i eth0`

### При помощи утилиты **traceroute** построить список маршрутизаторов на пути от ws11 до ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2077.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2078.png)

> Каждый пакет проходит на своем пути определенное количество узлов, пока достигнет своей цели. Причем, каждый пакет имеет свое время жизни. Это количество узлов, которые может пройти пакет перед тем, как он будет уничтожен. Этот параметр записывается в заголовке TTL, каждый маршрутизатор, через который будет проходить пакет уменьшает его на единицу. При TTL=0 пакет уничтожается, а отправителю отсылается сообщение Time Exceeded.
> 

> Команда traceroute linux использует UDP пакеты. Она отправляет пакет с TTL=1 и смотрит адрес ответившего узла, дальше TTL=2, TTL=3 и так пока не достигнет цели. Каждый раз отправляется по три пакета и для каждого из них измеряется время прохождения. Пакет отправляется на случайный порт, который, скорее всего, не занят. Когда утилита traceroute получает сообщение от целевого узла о том, что порт недоступен трассировка считается завершенной.
> 

### 5.6. Использование протокола **ICMP** при маршрутизации

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2079.png)

### Пропинговать с ws11 несуществующий IP (например, *10.30.0.111*) с помощью команды:

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2080.png)

## Part 6. Динамическая настройка IP с помощью **DHCP**

- `` Следующим нашим шагом будет более подробное знакомство со службой **DHCP**, которую ты уже знаешь.

**== Задание ==**

*В данном задании используются виртуальные машины из Части 5*

### Для r2 настроить в файле */etc/dhcp/dhcpd.conf* конфигурацию службы **DHCP**:

### 1) указать адрес маршрутизатора по-умолчанию, DNS-сервер и адрес внутренней сети. Пример файла для r2:

```
subnet 10.100.0.0 netmask 255.255.0.0 {}subnet 10.20.0.0 netmask 255.255.255.192
{    range 10.20.0.2 10.20.0.50;    option routers 10.20.0.1;    option domain-name-servers 10.20.0.1;}
```

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2081.png)

### 2) в файле *resolv.conf* прописать `nameserver 8.8.8.8.`

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2082.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2083.png)

### Указать MAC адрес у ws11, для этого в *etc/netplan/00-installer-config.yaml* надо добавить строки: `macaddress: 10:10:10:10:10:BA`, `dhcp4: true`

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2084.png)

### Для r1 настроить аналогично r2, но сделать выдачу адресов с жесткой привязкой к MAC-адресу (ws11). Провести аналогичные тесты

- В отчёте этот пункт описать аналогично настройке для r2.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2085.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2086.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2087.png)

### Запросить с ws21 обновление ip адреса

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2088.png)

Команда для смены присвоенного ip - dhclient, утилита для управления адресом интерфейса по протоколу DHCP.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2089.png)

### Сохранить дампы образов виртуальных машин

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2090.png)

## Part 7. **NAT**

- `` Ну и, наконец, в качестве вишенки на торте, я расскажу тебе про механизм преобразования адресов.

**== Задание ==**

*В данном задании используются виртуальные машины из Части 5*

### В файле */etc/apache2/ports.conf* на ws22 и r1 изменить строку `Listen 80` на `Listen 0.0.0.0:80`, то есть сделать сервер Apache2 общедоступным

сначала нжуно установить apache2 (sudo apt install apache2)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2091.png)

### Запустить веб-сервер Apache командой `service apache2 start` на ws22 и r1

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2092.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2093.png)

### Добавить в фаервол, созданный по аналогии с фаерволом из Части 4, на r2 следующие правила:

### 1) удаление правил в таблице filter - `iptables -F`

### 2) удаление правил в таблице "NAT" - `iptables -F -t nat`

### 3) отбрасывать все маршрутизируемые пакеты - `iptables --policy FORWARD DROP`

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2094.png)

### Запускать файл также, как в Части 4

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2095.png)

### Проверить соединение между ws22 и r1 командой `ping`

*При запуске файла с этими правилами, ws22 не должна "пинговаться" с r1*

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2096.png)

### Добавить в файл ещё одно правило:

### 4) разрешить маршрутизацию всех пакетов протокола **ICMP**

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2097.png)

### Сначала прописываем общую политику отбрасывать все маршрутизируемые пакеты, затем добавляем разрешение icmp-пакетов для прохода пинга. Без разрешения (на первом скрине) ws22 не пингуется r1, с разрешением (на втором скрине) пингуется.

### 

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2098.png)

### Добавить в файл ещё два правила:

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%2099.png)

### Запускать файл также, как в Части 4

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20100.png)

### Для следующей части задания я разрешил проходить tcp-пакетам через r2 и добавил к настройкам apache2 на ws22 прослушивание 8080 порта. Прописанные для SNAT и DNAT строчки в скрипте представлены на скрине. r1 подключается к ws22 и наоборот.

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20101.png)

## Part 8. Дополнительно. Знакомство с **SSH Tunnels**

- `` Пожалуй, на этом у меня всё. Может у тебя появились ещё какие-то вопросы?
- `` Да, я хотел спросить ещё об одной вещи. На работе я краем уха услышал, что в моей компании есть некие проекты по обучению. Подробностей я не знаю, но очень хочется взглянуть... Вдруг будет полезно
- `` Действительно интересно, но как в этом помогу тебе я?
- `` Дело в том, что, чтобы добраться до этих проектов, нужно получить доступ к закрытой сети. Можешь посоветовать что-нибудь по этому поводу?
- `` Ну ты, конечно, даёшь... Не уверен на все сто, что это поможет, но могу рассказать тебе про **SSH Tunnels**.

**== Задание ==**

*В данном задании используются виртуальные машины из Части 5*

### Запустить веб-сервер **Apache** на ws22 только на localhost (то есть в файле */etc/apache2/ports.conf* изменить строку `Listen 80` на `Listen localhost:80`)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20102.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20103.png)

ws21

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20104.png)

ws11

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20105.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20106.png)

![Untitled](linux_network%20v1%200%2097ab9a816ece41578dbbdffb6ac7ac88/Untitled%20107.png)

##
