FROM mcr.microsoft.com/devcontainers/python:0-3.10

ENV PYTHONUNBUFFERED=1
ENV DEBIAN_FRONTEND=noninteractive

# 💥 ELIMINA el repo roto de yarn
RUN rm -f /etc/apt/sources.list.d/yarn.list

# Ahora sí, instala sin errores
RUN apt-get update \
    && apt-get install -y --no-install-recommends postgresql-client \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*