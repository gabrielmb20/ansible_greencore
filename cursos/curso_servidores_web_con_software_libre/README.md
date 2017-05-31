# Ansible Greencore - Curso servidores web

Configura las aulas para el curso de servidores web basados en software libre

## Uso

Descargue el proyecto y entre en la carpeta de las recetas para este curso.
```bash
git clone https://github.com/fede2cr/ansible_greencore.git
cd cursos/curso_servidores_web_con_software_libre
```

Ahora puede ejecutar recetas de Ansible como:

Por lo menos para actualizar los equipos

```bash
ansible-playbook 00-setup-mirror.yml 01-upgrade.yml -i inventory/hosts.labXX
```

Se recomienda realizar las recetas bases, que preparan un aula para el curso en particular:

```bash
ansible-playbook 00-setup-mirror.yml  01-upgrade.yml  02-preparacion_labs.yml  03-configura-software.yml  04-configura-contenedores.yml -i inventory/hosts.labXX 
```

