# Basis Image
FROM python:alpine

# Lege den App-Code ins Verzeichnis /code innerhalb des Container-Images
ADD . /code

# Setze das Working-Verzeichnis für die folgenden Kommandos
WORKDIR /code

# Installiere die dependencies
RUN pip install -r requirements.txt

# Kommando soll ausgeführt werdne, wenn der Container startet
ENTRYPOINT ["python", "app.py"]