# Usa una imagen base de Node
FROM node:latest

# Crea un directorio de trabajo en el contenedor
WORKDIR /app

# Asegúrate de que la ruta a package.json sea la correcta
COPY frontend-bd/package*.json ./

# Instala las dependencias del proyecto
RUN npm install

# Copia los archivos y carpetas del proyecto al directorio de trabajo
# Asegúrate de que la ruta de origen refleje la nueva estructura
COPY frontend-bd/ .

# Expone el puerto en el que se ejecutará la aplicación React
EXPOSE 3000

# Define el comando para ejecutar la aplicación
CMD ["npm", "start"]