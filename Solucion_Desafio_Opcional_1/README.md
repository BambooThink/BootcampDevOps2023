# Solución Desafío Opcional No. 1

## Instalación de Grafana, Prometheus y Prometheus Node Exporter mediante Ansible

### Estructura de directorios

``` Markdown

SOLUCIÓN_DESAFíO_OPCIONAL_1/
├── config/
│   ├── node_exporter.service.j2
│   ├── prometheus.yml.j2
│   └── prometheus.service.j2
├── packages/
│   ├── grafana.yml
│   ├── node_exporter.yml
│   └── prometheus.yml
├── inventory.ini
├── main.yml
├── Solución_Desafio_Opcional_1_-_Marco_Vanegas.pdf
└── README.md

```

- #### Solución_Desafio_Opcional_1_-_Marco_Vanegas.pdf

    Este [archivo](Solución_Desafio_Opcional_1_-_Marco_Vanegas.pdf) contiene la documentación de la solución.

- #### config/

    Contiene los archivos de configuración de los servicios a instalar.

    - node_exporter.service.j2: Archivo de configuración del servicio node_exporter.
    - prometheus.yml.j2: Archivo de configuración de prometheus.
    - prometheus.service.j2: Archivo de configuración del servicio prometheus.

- #### packages/

    Contiene los archivos de instalación de los servicios a instalar.

    - grafana.yml: Archivo de instalación de grafana.
    - node_exporter.yml: Archivo de instalación de node_exporter.
    - prometheus.yml: Archivo de instalación de prometheus.

- #### inventory.ini

    Contiene la información de los hosts a configurar.

- #### main.yml

    Contiene las tareas a ejecutar.

- #### Comando de ejecución

    ``` bash
    ansible-playbook -i inventory.ini main.yml -u dev -K
    ```
    Dev es el usuario de la máquina remota y -K es para que solicite la contraseña de dicho usuario.
