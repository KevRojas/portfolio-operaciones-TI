# Servicios DHCP e IIS

## 1. Servicio DHCP

### Objetivo
Instalar y configurar el rol DHCP para la asignación
automática de direcciones IP a los clientes de la red.

### Configuración

| Parámetro | Valor |
|---|---|
| Ámbito | 192.168.20.2/24 |
| Rango de IPs | 192.168.20.10 - 192.168.20.100 |
| Puerta de enlace | 192.168.20.1 |
| DNS | 192.168.20.2 |
| Duración de concesión | 180 días |

### Comprobación

Se verificó desde Administrador DHCP la creación
de las IPs dentro del rango configurado.

### Evidencia

<img width="1191" height="830" alt="01-DHCP" src="https://github.com/user-attachments/assets/d74f4111-2266-4fad-ba27-44e70ad818cb" />


---

## 2. Servicio IIS (Servidor Web)

### Objetivo
Instalar el rol de Servidor Web (IIS) y publicar 5 sitios
web de prueba accesible desde la red interna.

### Configuración

| Parámetro | Valor |
|---|---|
| Nombre del sitio | cafeprincipal |
| Puerto | 80 |
| Ruta física | C:\inetpub\coffee |
| Binding | 192.168.20.2:80 |

| Parámetro | Valor |
|---|---|
| Nombre del sitio | navidadprincipal |
| Puerto | 80 |
| Ruta física | C:\inetpub\chrism |
| Binding | 192.168.20.3:80 |

| Parámetro | Valor |
|---|---|
| Nombre del sitio | mobilesprincipal |
| Puerto | 80 |
| Ruta física | C:\inetpub\uxos |
| Binding | 192.168.20.4:80 |

| Parámetro | Valor |
|---|---|
| Nombre del sitio | innovaprincipal |
| Puerto | 80 |
| Ruta física | C:\inetpub\innova |
| Binding | 192.168.20.5:80 |

| Parámetro | Valor |
|---|---|
| Nombre del sitio | escuelaprincipal |
| Puerto | 80 |
| Ruta física | C:\inetpub\school |
| Binding | 192.168.20.6:80 |

### Comprobación

Se verificó el acceso desde el navegador mostrando la
página de inicio del sitio publicado.

### Evidencia

<img width="1208" height="896" alt="02-IIS" src="https://github.com/user-attachments/assets/8ed2dbc3-f187-4263-a7fa-b506ea59a117" />

<img width="1220" height="869" alt="02-IIS-Coffee" src="https://github.com/user-attachments/assets/f5b2ab6b-9f1b-401e-9117-52c7f60993f4" />

<img width="1252" height="913" alt="03-IIS-School" src="https://github.com/user-attachments/assets/23de7a6d-ec7d-4118-a2db-5152b92869df" />

<img width="1251" height="901" alt="04-IIS-Innova" src="https://github.com/user-attachments/assets/7eaeffaf-654c-416f-a175-4d33058fca53" />

<img width="1225" height="905" alt="05-IIS-Mobile" src="https://github.com/user-attachments/assets/3fef7c61-d94b-4cb3-abe0-86673cbf5f59" />

<img width="1249" height="878" alt="06-IIS-Chrism" src="https://github.com/user-attachments/assets/5076708a-cf59-4d6e-b7ff-b3810667b794" />
