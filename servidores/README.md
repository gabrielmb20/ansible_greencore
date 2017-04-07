# Tareas comunes para ejecuta en un servidor

## Descripción:

Las siguientes recetas de Ansible están hechas para ejecutarse sobre un servidor Ubuntu instalado con solamente el paquete de ssh.

Algunas características del servidor final:

- Deshabilita Biosdevname
- Instala plantilla de interfaces de red con bridge y team
- Paquetes requeridos para contenedores LXC y virtualización KVM

## Instrucciones:

- Descargue las recetas de software, y entre al directorio específico para servidores

```bash
$ sudo apt-get install ansible git
$ git clone git@github.com:fede2cr/ansible_greencore.git
$ cd ansible_greencore/servidores
```
- Use como base los archivos en ../inventory/ para definir las direcciones de los equipos a administrar.
- Opcional: solo se encuentra dentro de Greencore. Realice un cambio para que se use el mirror local de Ubuntu/CentOS

```bash
$ ansible-playbook -i ../inventory/hosts.example -K 00-setup-mirror.yml
```
- Actualice los paquetes del equipo. Si usa paquetes de python, puede crear una regla similar para que mantenga actualizados los paquetes vía pip.
```bash
$ ansible-playbook -i ../inventory/hosts.example -K 01-upgrade.yml
```
- Instale paquetes base, y configuración inicial. Esto se definió para un servidor ejemplo, pero se recomienda crear recetas pra servidores específicos.
```bash
$ ansible-playbook -i ../inventory/hosts.example -K 02-base_setup.yml
```
