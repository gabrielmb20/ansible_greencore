# Instalación de curso de Untangle

Recetas de ansible para crear configuración de curso de Untangle, para impartir laboratorios prácticos del curso Administración de Plataforma Untangle, de Greencore Solutions SRL en Costa Rica.

## Descripción
Algunas de las operaciones que ejecuta la receta:
- 00 Mirror: Configura un mirror de Ubuntu para todos los equipos (físicos y contenedores)
- 01 Actualiza: Actualiza paquetes de Ubuntu de todos los equipos (físicos y contenedores)
- 02 Configura: Crea configuración de red en los equipos físicos, para virtualización y contenedores de LXC
- 03 Crea: Crea contenedores conectados a diferentes interfaces para manejo de contenido

## TODO
- [ ] Recetas para instalar Jupyter en los contenedores
- [ ] Receta para instalar contenido de libretas de Jupyter según el laboratorio a ejecutar
- [ ] Que los contenedores se agreguen automáticamente usando el módulo add_hosts de ansible
