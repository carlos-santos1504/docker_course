# backend/Dockerfile
FROM python:3.9-slim

# Definir o diretório de trabalho dentro do container
WORKDIR /app

# Copiar os arquivos do projeto para o diretório de trabalho
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

COPY . .

# Expor a porta 5000
EXPOSE 5000

# Comando para rodar o aplicativo
CMD ["python", "app.py"]
