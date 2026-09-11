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


# 1. `instalacion-ad-ds/`

# Instalación de Active Directory Domain Services

## Objetivo

Instalar el rol Active Directory Domain Services (AD DS)
en Windows Server y promover el servidor como controlador
de dominio.

## Entorno

- Windows Server
- VirtualBox
- Servidor: SERVER_OFICIAL
- Dominio: GRUPODOS.EDU.PE

## Requisitos previos

Antes de instalar AD DS se verificó:

- Nombre del servidor.
- Configuración de red.
- Dirección IP estática.
- Nombre del equipo.
- Conectividad de red.

## Procedimiento

### 1. Abrir Server Manager

Se accedió a Server Manager para agregar un nuevo rol.

<img width="1232" height="884" alt="01-ServerManager" src="https://github.com/user-attachments/assets/c1340e81-94fe-46c8-9bc1-ca97b38dc686" />


### 2. Instalar AD DS

Se seleccionó:

`Add Roles and Features`

Posteriormente se seleccionó:

`Active Directory Domain Services`

<img width="489" height="510" alt="02-ADDS" src="https://github.com/user-attachments/assets/8e9e67c0-a71b-4c68-9fbc-59630ec7c7ef" />


### 3. Promover el servidor

Después de instalar el rol se inició el proceso de
promoción del servidor a controlador de dominio.

<img width="544" height="403" alt="03-Dominio" src="https://github.com/user-attachments/assets/2247faa6-def4-496c-81b1-f3cc6a93dfef" />

<img width="544" height="403" alt="04-CreacionDominio" src="https://github.com/user-attachments/assets/d95d5f08-b2c1-474c-8041-3a0575fd04bb" />


### 4. Crear el dominio

Se creó el dominio de laboratorio:

```text
GRUPODOS.EDU.PE
```

<img width="1097" height="826" alt="05-LoginDominio" src="https://github.com/user-attachments/assets/f5e88fc5-cac6-44cb-9dfe-89f1315419ec" />
