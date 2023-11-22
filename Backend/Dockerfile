# Usa una imagen base de Python
FROM python:3.12

# Establece una variable de entorno que asegura que la salida de Python se envíe directamente a la terminal sin ser almacenada en buffer
ENV PYTHONUNBUFFERED 1

# Crea un directorio de trabajo en el contenedor
WORKDIR /app

# Copia el archivo requirements.txt en el contenedor
COPY requirements.txt .

# Instala las dependencias de Django
RUN pip install -r requirements.txt

# Copia los archivos y carpetas del proyecto al directorio de trabajo
COPY . .

# Expone el puerto para el servidor Django
EXPOSE 8000

# Define el comando para iniciar el servidor Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]