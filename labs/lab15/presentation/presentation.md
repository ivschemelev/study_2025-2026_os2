---
## Front matter
lang: ru-RU
title: Лабораторная работа №15
subtitle: Управление логическими томами (LVM)
author:
  - Щемелев Илья Владимирович
institute:
  - Российский университет дружбы народов, Москва, Россия

## Formatting pdf
toc: false
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

# Цель работы

## Формулировка цели

Получить навыки управления логическими томами LVM: создание PV/VG/LV, настройка монтирования и изменение размера логических томов и файловых систем.

# Ход выполнения работы

## Подготовка диска /dev/sdb под LVM

![Создание раздела /dev/sdb1 и назначение типа Linux LVM](Screenshot_1.png){ width=85% }

## Создание VG и LV (vgdata/lvdata)

![Создание VG vgdata, LV lvdata и файловой системы ext4](Screenshot_2.png){ width=85% }

## Постоянное монтирование /mnt/data

![Редактирование файла /etc/fstab для /mnt/data](Screenshot_3.png){ width=85% }

## Проверка монтирования /mnt/data

![Проверка монтирования логического тома в /mnt/data](Screenshot_4.png){ width=85% }

## Добавление нового PV в vgdata (/dev/sdb2)

![Создание /dev/sdb2 и проверка таблицы разделов /dev/sdb](Screenshot_5.png){ width=85% }

## Расширение группы томов vgdata

![Расширение vgdata: pvcreate, vgextend, контроль vgs/lvs/df](Screenshot_6.png){ width=85% }

## Увеличение lvdata и файловой системы ext4

![Увеличение lvdata и файловой системы (lvs/df -h)](Screenshot_7.png){ width=85% }

## Уменьшение lvdata и файловой системы ext4

![Уменьшение lvdata и проверка результата (lvs/df -h)](Screenshot_8.png){ width=85% }

# Самостоятельная работа

## Разметка диска /dev/sdc под LVM

![Проверка разметки диска /dev/sdc](Screenshot_9.png){ width=85% }

## Создание vggroup и lvgroup + XFS

![Создание PV/VG/LV и форматирование XFS](Screenshot_10.png){ width=85% }

## Проверка конфигурации LVM

![Проверка pvs/vgs/lvs](Screenshot_11.png){ width=85% }

## Постоянное монтирование /mnt/groups

![Настройка /etc/fstab для /mnt/groups](Screenshot_12.png){ width=85% }

## Проверка монтирования /mnt/groups

![Проверка mount и df -h для /mnt/groups](Screenshot_13.png){ width=85% }

## Расширение vggroup и lvgroup (XFS)

![Расширение vggroup/lvgroup и увеличение XFS](Screenshot_14.png){ width=85% }

## Итоговая проверка расширения

![Итоговая проверка pvs/vgs/lvs/df -h](Screenshot_15.png){ width=85% }

# Итоги работы

## Заключение

Выполнено создание физических томов, групп томов и логических томов LVM, настроено постоянное монтирование через `/etc/fstab`.  
Отработаны операции расширения и уменьшения логических томов с автоматическим изменением размера файловых систем **ext4** и **XFS**.  
Получены практические навыки гибкого управления дисковым пространством в Linux с использованием LVM.
