---
title: 'Проблемы при ручной установке сертификата на устройствах с Android 11 и новее'
taxonomy:
    category:
        - docs
visible: true
---

Чтобы иметь возможность фильтровать HTTPS-трафик (что крайне важно, так как большинство рекламы использует HTTPS), AdGuard необходимо установить сертификат в пользовательское хранилище сертификатов на вашем устройстве. На более старых версиях ОС Android это можно было сделать автоматически. На устройствах с версией Android 11 и новее требуется [ручная установка сертификата](https://kb.adguard.com/ru/android/overview#install-certificate).

<img src="https://cdn.adguard.com/public/Adguard/Blog/Android/3-5/cert-ru.gif" style="border: 1px solid #efefef; max-width: 350px; padding: 2px;">

Если во время ручной установки сертификата у вас возникли проблемы (например, вы установили сертификат,но приложение его игнорирует), ниже вы можете найти возможные пути решения.

<a id="secure-folder"></a>   

## Установка сертификата в "Папку Knox"

Если вы используете [Папку Knox/Защищенную папку](https://www.samsung.com/ru/support/mobile-devices/how-to-set-up-a-secure-folder/) (на более ранних версиях) на вашем Android (это в основном относится к устройствам Samsung), вы можете столкнуться с некоторыми трудностями при установке HTTPS-сертификата. Дело в том, что в *Папке Knox* есть собственное хранилище для сертификатов. Однако, когда вы скачиваете сертификат согласно [этой инструкции](https://kb.adguard.com/ru/android/overview#install-certificate), он устанавливается в основное хранилище устройства и не играет при этом никакой роли для приложения AdGuard в *Knox*. Чтобы справиться с этой проблемой и установить сертификат в хранилище *Папки Knox*, воспользуйтесь следующей инструкцией:

1. После установки приложения и подключения к VPN нажмите "Включить" рядом с надписью "HTTPS-фильтрация выключена". 
2. Затем нажмите "Далее" —> "Далее" —> "Сохранить его сейчас" —> "Разрешить".
3. Сохраните сертификат (на этом этапе можно его переименовать, чтобы было проще найти).
4. После появления экрана "Как установить сертификат?" НЕ нажимайте "Открыть настройки".
5. Сверните приложение и перейдите в *Папку Knox*.
6. Нажмите на три точки и перейдите в дополнительные настройки безопасности.
7. Нажмите "Установить из памяти" —> "Сертификат CA" —> "Установить в любом случае" —> Введите графический рисунок/пароль/отпечаток —> В нужной папке найдите сохранённый сертификат и выберите его.
8. Вернитесь в приложение AdGuard и закройте окно "Как установить сертификат?", нажав на крестик.
9. Готово! Сертификат установлен.