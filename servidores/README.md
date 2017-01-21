# Tareas comunes para ejecuta en un servidor

## Descripción:

Las siguientes recetas de Ansible están hechas para ejecutarse sobre un servidor Ubuntu instalado con solamente el paquete de ssh.

Algunas características del servidor final:

- Deshabilita Biosdevname
- Instala plantilla de interfaces de red con bridge y team
- Paquetes requeridos para contenedores LXC y virtualización KVM

## Instrucciones:

```
$ sudo apt-get install ansible git
$ git clone git@github.com:fede2cr/ansible_recipes.git
$ cd ansible_recipes/greencore_common
## Opcional, solo se encuentra dentro de Greencore
$ ansible-playbook -i ../inventory/hosts.example -K 00-setup-mirror.yml
## Actualiza luego de instalación 
$ ansible-playbook -i ../inventory/hosts.example -K 01-upgrade.yml
## Instala paquetes requeridos y configuración inicial
$ ansible-playbook -i ../inventory/hosts.example -K 02-base_setup.yml
```

Para consultas favor escribir a a alvaro@greencore.co.cr o soporte@greencore.co.cr
