FROM python:3.8-slim

RUN pip3 install --upgrade pip
RUN apt-get update

WORKDIR /app
COPY . /app

RUN pip3 install -r /app/requirements.txt
RUN pip3 install torch


# --- Auto-Generated Entrypoint Configuration ---
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
RUN mkdir -p /var/log && touch /var/log/app.log
EXPOSE 8900
ENTRYPOINT ["/entrypoint.sh"]
