# Documentación del Pipeline de Backend

Este documento describe los pasos y secretos necesarios para el pipeline de GitHub Actions del backend.

## Pasos del Pipeline

### 1. Tests de Backend
- **Descripción**: Ejecuta los tests para asegurar la calidad del código.
- **Comando**: `npm test`
- **Ubicación**: Directorio `backend`

### 2. Generación del Build
- **Descripción**: Compila el código para producción.
- **Comando**: `npm run build`
- **Ubicación**: Directorio `backend`

### 3. Despliegue en AWS EC2
- **Descripción**: Despliega la aplicación en una instancia EC2.
- **Proceso**:
  1. Configura credenciales AWS
  2. Establece conexión SSH
  3. Actualiza el código
  4. Reinstala dependencias
  5. Reinicia la aplicación con PM2

## Secretos Necesarios

### AWS Credentials
- **AWS_ACCESS_KEY_ID**: ID de la clave de acceso de AWS
- **AWS_SECRET_ACCESS_KEY**: Clave secreta de acceso de AWS
- **AWS_REGION**: Región de AWS donde está la instancia EC2

### EC2 Configuration
- **EC2_SSH_KEY**: Clave SSH privada para acceder a la instancia
- **HOST_DNS**: DNS público de la instancia EC2
- **USERNAME**: Nombre de usuario de la instancia EC2

## Trigger del Pipeline
El pipeline se ejecuta cuando:
- Se abre un Pull Request
- Se actualiza un Pull Request existente
- Se hace push a cualquier rama excepto main
