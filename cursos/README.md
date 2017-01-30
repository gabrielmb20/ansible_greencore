# Recetas de Ansible para Cursos

Recetas de Ansible que nos ayudan a preparar las aulas para los cursos que se desarrollan en Greencore Solutions

## Descripción

- preparacion_labs.yml: Configura, actualiza, instala aplicaciones requeridas para los cursos bases de Greencore
- curso_untangle/: Configura bridge, equipos virtuales y contenedores para curso del firewall UTM Untangle

## Uso
Realizar el siguiente procedimiento desde la estación de trabajo de un técnico:
Necesario:
- [x] Instalar paquete de git
- [x] Instalar paquete de ansible
- [x] Tener generada llave de SSH
- [x] Haber copiado la lave usando ```ssh-copy-id```, a los equipos a administrar

```
$ git clone https://github.com/fede2cr/ansible_greencore.git
$ cd ansible_greencore
$ ansible-playbook -i inventory/hosts.example-lab cursos/preparacion_labs.yml -K
```
