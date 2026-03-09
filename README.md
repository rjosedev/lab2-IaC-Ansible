# Sistema de automatización de equipos de red

## Network Automation Engineer - UTNFRC

## Descripción General

Este proyecto implementa una solución avanzada de automatización de red basado en los conceptos que se plantean en el campo de la Infraestructura como Código

## Metadatos del Proyecto

- **Proyecto**: Simulacro de Caso de Uso
- **Versión**: 1.0
- **Autor**: Roman Jose Ballesteros
- **Fecha de Creación**: 2025-10-23
- **Python Requerido**: >= 3.12

## Tecnologías utilizadas

- **VSC**: IDE para desarrollo de software
- **UV**: Package manager que permite la administración de paquetes y proyectos
- **Jinja2**: Templating engine para generar plantillas de configuraciones
- **EVE-NG**: Emulador Virtual Enviroment para desplegar e interconectar dispositivos de red
- **Cisco vIOS images**: Imagenes virtuales de IOS basadas en dispositivos Cisco
- **VMware Workstation**: Hipervisor tipo 2 para despliegue de VM EVE-NG
- **Git y Github**: Herramientas para control de cambios de proyectos de software
- **JSON**: Notación de Objetos JavaScript, es un formato de texto ligero y fácil de leer por humanos y máquinas, utilizado para intercambiar datos de manera estructurada
- **YAML**: Formato de serialización de datos legible por humanos, utilizado para escribir archivos de configuración, nuestro Modelo de datos
- **Paramiko**: Libreria de Python para gestionar conexiones SSH hacia cada dispositivo
- **Netmiko**: Libreria basada en Paramiko que simplifica la automatización de la gestión de dispositivos de red
- **Ansible**: Herramienta de automatización de código abierto diseñada para simplificar la gestión de configuraciones, el despliegue de aplicaciones y la orquestación de tareas de IT

## Desarrollo en Ansible

- **Playbook**: Un Ansible Playbook es un archivo de configuración escrito en YAML que define, de forma simple y legible, una serie de tareas automatizadas para ser ejecutadas en servidores remotos. Actúa como un "plano técnico" que indica qué acciones realizar (instalar software, copiar archivos, etc.) para alcanzar un estado deseado en la infraestructura
- **Inventario**: Un inventario de Ansible es un archivo de texto (generalmente en formato YAML o INI) que funciona como una lista organizada de los servidores o máquinas ("hosts") que quieres gestionar. Define las direcciones IP o nombres de dominio de tus equipos y permite agruparlos lógicamente para aplicar tareas, configuraciones o despliegues automáticos sobre subconjuntos específicos de infraestructura
- **Modelo de datos/Source of truth**: El modelo de datos de Ansible se basa en una estructura simple y legible, principalmente en formato YAML. Utiliza inventarios (listas de servidores), variables (definición de valores) y facts (datos del sistema recopilados) para definir el estado deseado de la infraestructura de forma declarativa y sin agentes
- **Templates**: Las plantillas (templates) de Ansible son archivos de configuración (generalmente con extensión .j2 para Jinja2) que permiten crear archivos dinámicos en los servidores de destino. Usan variables y lógica (bucles/condicionales) para personalizar el contenido automáticamente, facilitando la gestión de múltiples entornos sin editar archivos manualmente
- **Roles**: Un rol de Ansible es una forma estructurada y reutilizable de organizar tareas, variables, archivos y plantillas para automatizar configuraciones específica. Permite agrupar automatizaciones en carpetas, facilitando compartir y reutilizar código en distintos playbooks, haciéndolos más modulares y ordenados
- **Handlers**: Un handler en Ansible es una tarea especial que solo se ejecuta cuando otra tarea le envía una notificación ("notify") de que ha ocurrido un cambio (por ejemplo, al modificar un archivo de configuración)
- **Loop/When**: En Ansible, combinar loop con when permite iterar sobre una lista de elementos (con loop y {{ item }}) y aplicar una condición (when) para ejecutar la tarea solo en elementos específicos, saltando el resto. Es una forma eficiente de automatizar tareas repetitivas selectivamente
- **Tags**: Las etiquetas (tags) en Ansible son metadatos asignados a tareas o roles en un playbook que permiten ejecutar u omitir secciones específicas selectivamente. Actúan como filtros para correr solo una parte de la automatización en lugar del playbook completo, optimizando tiempo y permitiendo precisión quirúrgica
- **Vault**: Ansible Vault es una funcionalidad integrada en Ansible que permite cifrar archivos, variables o secretos confidenciales (contraseñas, claves API) dentro de los proyectos de automatización. Utiliza cifrado simétrico AES256, asegurando que los datos sensibles estén protegidos en reposo, pero puedan descifrarse automáticamente durante la ejecución de playbooks
- **Validación**: La validación de JSON Schema en Ansible asegura que los datos estructurados (variables, archivos de configuración) cumplan con un formato predefinido, evitando errores en la automatización
- **Documentación**: Playbook para creación de archivos .MD asociados a cada dispositivo del inventario con la descripción de las configuraciones aplicadas en el dispositivo

## Topología de red

![Topología de red lab2](/media/Screenshot from 2026-01-06 07-45-20.png)


