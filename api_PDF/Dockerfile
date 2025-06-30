FROM python:3.11-slim

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia todo el contenido del folder actual al contenedor
COPY . .

# Instala las dependencias necesarias
RUN pip install --no-cache-dir -r requirements.txt

# Crea el folder temporal donde se guardan los PDF si no existe
RUN mkdir -p /app/temp

# Expone el puerto donde se ejecutará la API
EXPOSE 8000

# Comando para iniciar la aplicación con Uvicorn
CMD ["uvicorn", "main:app", "--host=0.0.0.0", "--port=5025", "--reload"]
