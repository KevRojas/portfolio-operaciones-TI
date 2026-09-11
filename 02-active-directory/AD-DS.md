# Active Directory

## Objetivo

Implementar y administrar un entorno de Active Directory
utilizando Windows Server, con el objetivo de practicar
tareas relacionadas con la administración de usuarios,
grupos, equipos, políticas y resolución de incidencias.

## Entorno de laboratorio

| Componente | Configuración |
|---|---|
| Hipervisor | VirtualBox |
| Servidor | Windows Server |
| Cliente | Windows 7 |
| Dominio | GRUPODOS.EDU.PE|
| Controlador de dominio | Administrador |
| DNS | Administrador |
| Red | 192.168.20.2/24 |

## Arquitectura

```text
              SERVER_OFICIAL
              Windows Server
                    │
        ┌───────────┼───────────┐
        │           │           │
       AD DS       DNS          GPO
        │
   ┌────┴─────┐
   │          │
Usuarios    Grupos
   │          │
   ▼          ▼
lesquen    CIBERTEC_LIMA
Windows 7

kevin
Windows 10

```
