команда для запуска: ansible-playbook -i inventory/prod/hosts.yml site.yml --ask-become-pass


play для elasticsearch:

    0. перезагрузка elasticsearch
    1. загрузка deb пакета в случае если его нет локально
    2. установка
    3. настройка конфигурации elasticsearh (если были изменения в файлах конфигурации - вызов пункта 0)


play для kibana:

    0. перезагрузка kibana
    1. загрузка deb пакета в случае если его нет локально
    2. установка
    3. настройка конфигурации kibana (если были изменения в файлах конфигурации - вызов пункта 0)
  
  play для filebeat:

    0. перезагрузка filebeat
    1. загрузка deb пакета в случае если его нет локально
    2. установка
    3. настройка конфигурации filebeat (если были изменения в файлах конфигурации - вызов пункта 0)
    4. запуск модуля system для того чтобы filebeat забирал системные логи
    5. передача данных в kibana 
  


