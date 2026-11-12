# Nodo Cero

## Nombre y descripción del proyecto

- **Proyecto:** Nodo Cero
- **Alumno:** Hugo Fernández Tarazón
- **Ciclo:** 2.º de Administración de Sistemas Informáticos en Red (ASIR)
- **Centro:** IES Conselleria

Nodo Cero es un proyecto académico de una empresa orientada a ofrecer servicios informáticos y de ciberseguridad a pequeñas y medianas empresas (PYMES) de la Comunitat Valenciana. La propuesta contempla el diseño, despliegue, administración y mantenimiento de una infraestructura tecnológica segura, eficiente y escalable.

## Objetivo de la infraestructura

Disponer de una infraestructura centralizada y segmentada que permita alojar y administrar los servicios de la empresa de forma segura y fiable. Los objetivos principales son:

- Centralizar los servicios y facilitar su administración.
- Segmentar la red mediante VLAN para limitar los accesos entre redes.
- Proteger los servicios mediante firewall, proxy inverso y acceso remoto VPN.
- Automatizar configuraciones y tareas repetitivas.
- Supervisar la disponibilidad, el rendimiento y el consumo de recursos.
- Realizar copias de seguridad y facilitar la recuperación ante incidencias.
- Mantener la documentación y el historial de cambios mediante Git.

La arquitectura se plantea como una propuesta académica para una PYME de referencia de 25 usuarios. Antes de un despliegue real habría que validar y ajustar sus requisitos.

## Tecnologías utilizadas

| Tecnología | Función |
|---|---|
| Proxmox VE (KVM y LXC) | Virtualización y gestión de máquinas virtuales y contenedores. |
| Debian 13 GNU/Linux | Sistema operativo base de los servidores. |
| Nginx | Servidor web y proxy inverso. |
| PostgreSQL | Sistema gestor de bases de datos. |
| Docker | Ejecución de aplicaciones en contenedores. |
| Ansible | Automatización de configuración y administración. |
| pfSense | Firewall, filtrado de tráfico y VPN. |
| Prometheus y Grafana | Monitorización, métricas y paneles. |
| Proxmox Backup Server y scripts TAR | Copias de seguridad y recuperación. |
| Git y GitHub | Control de versiones y alojamiento del repositorio. |

## Estructura del repositorio

```text
nodo_cero/
├── playbooks/
│   └── site.yml
├── roles/
│   ├── seguridad/
│   ├── monitorizacion/
│   ├── servicios_web/
│   └── firewall/
├── variables/
├── plantillas/
├── inventario/
├── documentacion/
└── README.md
```

- **playbooks/**: playbooks principales de Ansible para coordinar el despliegue.
- **roles/**: tareas y configuraciones separadas por función.
- **variables/**: variables generales y específicas de los entornos.
- **plantillas/**: plantillas de configuración procesables con Ansible.
- **inventario/**: inventarios de hosts y grupos de servidores.
- **documentacion/**: memoria técnica, diagramas, procedimientos y evidencias.
- **README.md**: descripción general, objetivos, tecnologías y organización del repositorio.

## Uso inicial

El playbook principal está en `playbooks/site.yml`. Antes de ejecutarlo, revisa el inventario y adapta las variables y los equipos al laboratorio. Ejecuta las pruebas únicamente sobre sistemas propios o para los que tengas autorización.

Este repositorio forma parte del **Proyecto Intermodular de 2.º ASIR** y se ampliará conforme avance el diseño y la implantación del laboratorio de Nodo Cero.
