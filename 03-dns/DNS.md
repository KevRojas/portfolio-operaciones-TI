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
| DESKTOP-8C321AK | 192.168.20.10 | Cliente Windows 10|
| kevin-pc | 192.168.20.11 | Cliente Windows 7 |

## Zona DNS

Se verificó la existencia de la zona DNS correspondiente
al dominio:

<img width="1128" height="816" alt="01-DNS" src="https://github.com/user-attachments/assets/0316681f-68dc-4f68-afb2-f4b25c32eb72" />

<img width="1167" height="675" alt="03-ClienteW10" src="https://github.com/user-attachments/assets/8da142eb-ef53-4739-930a-5f526d3be522" />

<img width="1161" height="813" alt="04-ClienteW7" src="https://github.com/user-attachments/assets/99ac03c4-4289-4b37-a87a-55d227ef4329" />
