# Usa Node 20 come immagine base
FROM node:20

# Imposta la directory di lavoro
WORKDIR /workspace

RUN apt-get update && apt-get install -y git

# Installa e configura pnpm
RUN npm install -g pnpm \
    && pnpm config set store-dir /root/.local/share/pnpm/store \
    && mkdir -p /root/.local/share/pnpm/store \
    && chmod -R 777 /root/.local/share/pnpm

# Installa firebase-tools globalmente
RUN npm install -g firebase-tools

# Configura pnpm per una migliore compatibilità con npm
ENV PNPM_HOME="/root/.local/share/pnpm"
ENV PATH="${PATH}:${PNPM_HOME}"

# Imposta le configurazioni di pnpm per il progetto
RUN pnpm config set shamefully-hoist true \
    && pnpm config set strict-peer-dependencies false \
    && pnpm config set node-linker hoisted

# Non installiamo Vite globalmente poiché lo aggiungeremo come devDependency nel package.json

# Pulisci la cache di npm per ridurre la dimensione dell'immagine
RUN npm cache clean --force \
    && rm -rf /root/.npm/_cacache

# Imposta le permission corrette per la directory di lavoro
RUN chmod -R 777 /workspace