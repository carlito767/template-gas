FROM node:18.17.1-buster

# Args
ARG PNPM_VERSION=8.6.12

# Envs
ENV PNPM_VERSION=${PNPM_VERSION}
ENV PNPM_HOME=/usr/local/bin

# Set working directory
WORKDIR /workspace

# Copy configuration files
COPY .npmrc pnpm-lock*.yaml ./

# Update npm
RUN npm i -g npm@latest && \
  # Install pnpm
  npm install -g pnpm@$PNPM_VERSION &&\
  # Config store
  pnpm config set store-dir .pnpm-store &&\
  # Fetch packages from lockfile into virtual store, package manifest is ignored
  pnpm fetch &&\
  # Install dependencies from virtual store
  pnpm install -r --offline &&\
  # Install global dependencies
  # clasp 2.4.0 instead of latest, see https://github.com/google/clasp/issues/869
  pnpm add -g @google/clasp@2.4.0 &&\
  # jest
  pnpm add -g jest@v29.6.4

# Copy project files
COPY . ./
