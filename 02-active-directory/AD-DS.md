# `ACTIVE DIRECTORY`

## Objetivo

Implementar y administrar un entorno de Active Directory
utilizando Windows Server, con el objetivo de practicar
tareas relacionadas con la administración de usuarios,
grupos, dominios, políticas y resolución de incidencias.

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
                            │           │           │ 
                            │           │        Quitar y evitar el acceso
                            │           │        a los comandos Apagar, Reiniciar,
                            │           │        Suspender e Hibernar.
                            │           │
                            │           │
                            │      192.168.20.2
                            │
                       ┌────┴─────┐
                       │          │
                    Usuarios    Grupos
                       │          │
                       ▼          ▼
            GRUPODOS/lesquen    CIBERTEC_LIMA
                    Windows 7    
            GRUPODOS\kevin
                    Windows 10


```


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

<img width="916" height="477" alt="06-Comprobación" src="https://github.com/user-attachments/assets/ab405259-2d87-41d4-b96c-dd0d14d99c01" />



# Administración de usuarios en Active Directory

## Objetivo

Practicar la creación, modificación, bloqueo, desbloqueo,
habilitación y deshabilitación de cuentas de usuario mediante
Active Directory Users and Computers.

## Entorno

- Windows Server
- Active Directory Domain Services
- Dominio: `GRUPODOS`
- Domain Controller: `SERVER_OFICIAL`

## Usuarios de laboratorio

| Nombre | Usuario | Área | OU |
|---|---|---|---|
| Everli Cruzado | ecruzado | CIBERTEC_LIMA | INDEPENDENCIA |
| Jorge Pisco | jpisco | CIBERTEC_LIMA | INDEPENDENCIA |
| Luis Esquen | lesquen | CIBERTEC_LIMA | INDEPENDENCIA |

## 1. Creación de usuario

Se creó usuarios de prueba dentro de la OU correspondiente.

### Datos del usuario

```text
Nombre: Luis Esquen
Usuario: lesquen
Área: CIEBRTEC_LIMA
OU: INDEPENDENCIA
```

<img width="921" height="551" alt="07-CreacionUsers" src="https://github.com/user-attachments/assets/4fabfeab-d61b-42e8-b511-1509a2be050a" />


# Administración de grupos en Active Directory

## Objetivo

Practicar la creación y administración de grupos de seguridad
en Active Directory y la asignación de usuarios como miembros.

## Entorno

- Windows Server
- Active Directory Domain Services
- Dominio: `GRUPODOS`
- Domain Controller: `SERVER_OFICIAL`

## Grupos de laboratorio

| Grupo | SubGrupo |
|---|---|
| CIBERTEC_LIMA | BREÑA - CALLAO - INDEPENDENCIA - LC - SJL|


## Creación de grupo

Se creó el grupo:

```text
CIBERTEC_LIMA
```

<img width="234" height="186" alt="08-Grupos" src="https://github.com/user-attachments/assets/f50ea021-b942-46d8-8f7b-f473de6fb25d" />


# Administración de GPO en Active Directory

## Objetivo

Crear, configurar y aplicar directivas de grupo (Group Policy
Objects - GPO) en un entorno de Active Directory, con el objetivo
de administrar configuraciones de usuarios y equipos de forma
centralizada.

## Entorno

- Windows Server
- Active Directory Domain Services
- Group Policy Management
- Dominio: `GRUPODOS`
- Domain Controller: `SERVER_OFICIAL`
- Cliente: `kevin`
- Sistema cliente: Windows 10

## Conceptos básicos

Una GPO permite administrar de forma centralizada diferentes
configuraciones de los equipos y usuarios pertenecientes a un
dominio.

Las políticas pueden aplicarse a:

- Usuarios.
- Equipos.
- Unidades Organizativas (OU).
- Dominio completo.

## GPO implementadas

Para este laboratorio se configuraron las siguientes políticas:

| GPO | Objetivo |
|---|---|
| GPO upn | Quitar y evitar el acceso a los comandos Apagar, Reiniciar, Suspender e Hibernar. |

# Creación de una GPO

## Objetivo

Crear una nueva GPO y vincularla a una Unidad Organizativa.

<img width="787" height="503" alt="09-GPO" src="https://github.com/user-attachments/assets/c0c0cef9-bc4d-4a9d-9dbc-9e57127b6326" />

## Procedimiento

1. Abrir Herramientas y luego **Administración de directivas de grupo**.
2. Seleccionar el dominio `GRUPODOS`.
3. Seleccionar la OU correspondiente.
4. Crear una nueva GPO.
5. Asignar un nombre descriptivo.

## Demostración

<img width="481" height="643" alt="10-Demostracion" src="https://github.com/user-attachments/assets/e9021fd4-716b-44f6-a56e-dabf1faecc92" />

