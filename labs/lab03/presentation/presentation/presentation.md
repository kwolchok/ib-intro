---
## Front matter
lang: ru-RU
title: "Лабораторная работа №3"
subtitle: "Информационная безопасность "
author: "Волчок Кристина Александровна НПМбд-02-21"

institute:
  - Российский университет дружбы народов, Москва, Россия
  
date:  19 сентября 2024

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---



## Объект и предмет исследования
Объект исследования:

Права доступа пользователей в операционной системе Linux и управление ими через создание учетных записей и групп.

Предмет исследования:
Исследование порядка создания учетных записей, назначения паролей и прав доступа, а также взаимодействие пользователей в различных группах. Проверка возможности выполнения различных операций (создание, удаление, изменение файлов и директорий) при изменении атрибутов доступа к файлам и директориям для пользователей группы и сравнение минимально необходимых прав для этих операций.

## Цели и задачи

Получение практических навыков работы в консоли с атрибутами файлов для групп пользователей1.

## Материалы и методы



### Материалы:
1. Операционная система Linux, установленная в виртуальной или физической среде.
2. Пользовательские учетные записи администратора и двух обычных пользователей (`guest` и `guest2`).
3. Командная строка (терминал) для выполнения операций с пользователями и правами.

### Методы:
1. **Создание учетных записей пользователей**: 
   Создание новых пользователей `guest` и `guest2` выполнялось с использованием команды `useradd`. Для установки пароля использовалась команда `passwd`.

2. **Назначение прав доступа и управление группами**: 
   Пользователь `guest2` был добавлен в группу `guest` командой `gpasswd -a`. Команда `newgrp` использовалась для регистрации пользователя в группе.

3. **Работа с правами доступа к директориям и файлам**: 
   Права доступа для директории `/home/guest` были изменены с использованием команды `chmod`, чтобы разрешить выполнение всех операций для группы. Дополнительно атрибуты директории `/home/guest/dir1` были полностью сняты командой `chmod 000`, а затем проверено, какие действия разрешены пользователю `guest2`.




## Результаты

В ходе работы были созданы учетные записи пользователей `guest` и `guest2`, настроены права доступа и проведено управление группами. Это позволило проверить выполнение базовых операций пользователями в зависимости от установленных прав.

Права на директорию `/home/guest` были изменены для разрешения всех действий группе. Пользователь `guest2` смог выполнять операции, такие как создание и удаление файлов.

После снятия всех атрибутов с директории `/home/guest/dir1` доступ к файлам был заблокирован, что подчеркнуло важность правильной настройки прав.

Проверка минимально необходимых прав для выполнения операций, таких как создание, удаление, чтение и запись файлов, показала, что для создания файлов необходимы права `d-wx`.

Сравнение с предыдущей лабораторной работой подтвердило, что основное изменение связано с невозможностью изменения атрибутов файлов из-за отсутствия прав у пользователя. Остальные операции выполняются корректно в соответствии с правами.

Результаты показали зависимость возможностей выполнения операций от установленных прав и важность корректной настройки прав доступа в Linux.


## Вывод:
Точное управление правами доступа пользователей и групп в операционной системе Linux играет важную роль в обеспечении безопасности системы и организации работы с файлами и директориями.

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Волчок Кристина Александровна, студентка  кафедры прикладной информатики и теории вероятностей
  * Российский университет дружбы народов
  * [1032215007@rudn.ru]
:::
::: {.column width="30%"}



:::
::::::::::::::
