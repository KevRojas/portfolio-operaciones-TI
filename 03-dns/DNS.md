
# DNS

# Administración de DNS en Windows Server

## Objetivo

Configurar y comprobar el funcionamiento del servicio DNS
en Windows Server dentro de un entorno de Active Directory.

## Entorno

- Windows Server
- DNS Server
- Active Directory
- Domain Controller: `SERVER_OFICIAL`
- Dominio: `GRUPODOS`
- Red: `192.168.20.2/24`

## Configuración de red

| Equipo | Dirección IP | Función |
|---|---|---|
| SERVER_OFICIAL | 192.168.20.2 | DNS / Domain Controller |
| KEVIN | 192.168.20.10 | Cliente Windows 10|
| lesquen | 192.168.20.11 | Cliente Windows 7 |

## 1. Zona DNS

Se verificó la existencia de la zona DNS correspondiente
al dominio:

```text
empresa.test

