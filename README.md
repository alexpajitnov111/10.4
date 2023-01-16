10.4 Резервное копирование

Задание 1
В чём разница между: полным резервным копированием, дифференциальным резервным копированием, инкрементным резервным копированием.
Full BackUp делает полное копирование всего, самый долгий вариант резервного копирования с точки зрения процесса, дает нагрузку на диски и на сеть (если она сетевая), самый надежный и быстрый с точки зрения восстановления данных.
При дифференциальном резервном копировании сначала делается полное резервное копирование, затем при каждом запуске процесса резервируются только измененные данные, но точкой отсчета является состояние времени полного бэкапа. Такое резервное копирование быстрее, чем полное, но медленнее, чем инкрементное. Восстановление наоборот. Памяти на определенный период меньше, чем у полного, но
больше, чем у инкрементного.
Инкрементное копирование работает как дифференцированное копирование, но в отличии от него бэкапятся данные, которые были изменены из последнего слепка, то есть отправная точка каждого нового бэкапа это бэкап n-1.

Задание 2
Установите программное обеспечении Bacula, настройте bacula-dir, bacula-sd, bacula-fd. Протестир2уйте работу сервисов. Пришлите конфигурационные файлы для bacula-dir, bacula-sd, bacula-fd.

**![bacula-dir.conf](https://github.com/alexpajitnov111/10.4/blob/main/bacula-dir.conf)**
**![bacula-fd.conf](https://github.com/alexpajitnov111/10.4/blob/main/bacula-fd.conf)**
**![bacula-sd.conf](https://github.com/alexpajitnov111/10.4/blob/main/bacula-sd.conf)**


Задание 3
Установите программное обеспечении Rsync. Настройте синхронизацию на двух нодах. Протестируйте работу сервиса. Пришлите рабочую конфигурацию сервера и клиента Rsync.

**![rsyncd.conf](https://github.com/alexpajitnov111/10.4/blob/main/rsyncd.conf)**
**![backup-node1.sh](https://github.com/alexpajitnov111/10.4/blob/main/backup-node1.sh)**
