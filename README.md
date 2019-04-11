GitLab
======

Для запуска GitLab необходимо в файле .env заполнить значения переменных

        SCHEME=http
        DOMAIN=site.local
        HOSTNAME=gitlab.site.local
        
Для запуска GitLab так же необходима внешняя сеть с названием gitlab

        docker network create gitlab
        
Внешняя сеть должна быть подключена к traefik для обеспечения доступа

        docker network connect gitlab <traefik-container>
        
Traefik можно взять [здесь](https://github.com/maxim-avramenko/traefik)