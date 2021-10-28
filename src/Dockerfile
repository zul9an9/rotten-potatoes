# imagem base
FROM python:3.8-slim-buster
# criar diretório dentro da imagem do container
WORKDIR /app

# copiar o arquivo de softwares neccessários 
COPY requirements.txt /app

# instalar o python
RUN python -m pip install -r requirements.txt

# copiar o aplicativo
COPY . /app

# expor a porta 5000
EXPOSE 5000

# executar o app
CMD ["gunicorn", "--workers=1", "--bind", "0.0.0.0:5000", "app:app"]