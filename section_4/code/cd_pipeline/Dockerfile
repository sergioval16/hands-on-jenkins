# Base image
FROM alpine:3.7

# Instalar Python 3 y pip
RUN apk add --update python3 py3-pip

# Actualizar pip a la última versión
RUN pip3 install --upgrade pip

# Copiar el archivo de dependencias
COPY requirements.txt /usr/src/app/

# Instalar dependencias usando la versión actualizada de pip
RUN pip3 install --no-cache-dir -r /usr/src/app/requirements.txt

# Copiar archivos de la aplicación
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/

# Exponer el puerto 5000
EXPOSE 5000

# Ejecutar la aplicación
CMD ["python3", "/usr/src/app/app.py"]
