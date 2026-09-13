# Rocky Linux – Prácticas básicas de administración

## Objetivo

Practicar tareas básicas de administración y soporte en un servidor Rocky Linux.

## Entorno

- Sistema operativo: Rocky Linux
- Entorno: Máquina virtual
- Uso: laboratorio personal

---

## Práctica 1: Navegación y administración de archivos

### Consultar directorio actual

```bash
pwd
```

### Listar archivos

```bash
ls
```

### Crear directorio

```bash
mkdir laboratorio
```

### Crear archivo

```bash
touch laboratorio/prueba.txt
```

### Escribir información

```bash
echo "Práctica Rocky Linux" > laboratorio/prueba.txt
```

### Consultar contenido

```bash
cat laboratorio/prueba.txt
```

<img width="1050" height="722" alt="01-PracticaNavegación" src="https://github.com/user-attachments/assets/ca84607d-6ef7-4aee-bfbe-305ca3713eb0" />

<img width="994" height="629" alt="02-EvidenciaNavegación" src="https://github.com/user-attachments/assets/27e52f22-d3d0-4889-9f2b-ea0d22786dc1" />


## Práctica 2: Usuarios y permisos

```bash
sudo useradd Soporte1
```

### Asignar contraseña

```bash
sudo passwd soporte
```

### Consultar usuario

```bash
id Soporte1
```

### Archivo de pruena

```bash
sudo touch /home/Soporte1/prueba.txt
```

### Cambiar propietario

```bash
sudo chown Soporte1:Soporte1 /home/Soporte1/prueba.txt
```

### Consultar permisos

```bash
ls -l /home/Soporte1/prueba.txt
```

<img width="1017" height="709" alt="03_CreacionUsuario" src="https://github.com/user-attachments/assets/ae4bbb9b-9c3f-4ae3-8610-6710d46f45e6" />

<img width="994" height="696" alt="04-Navegacion" src="https://github.com/user-attachments/assets/45e43f7e-83de-446b-84f8-9a89927752d6" />

<img width="928" height="281" alt="05-NuevoPsswd" src="https://github.com/user-attachments/assets/84a9f7b6-1e34-4271-b0a1-09be17873c94" />
