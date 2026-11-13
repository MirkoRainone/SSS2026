FROM python:3.11-slim

WORKDIR /app

# Copia e installa le dipendenze
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copia il resto del codice backend
COPY . .

# Espone la porta di default di FastAPI/Uvicorn
EXPOSE 8000

# Avvia il server rendendolo accessibile dall'esterno del container
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]