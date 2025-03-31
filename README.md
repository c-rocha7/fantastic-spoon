# Autenticação de Usuários

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

## 1. Descrição

O projeto Autenticação de Usuários é um teste tecnico no qual me foi passado onde devere ocorrer a autenticação de usuário com CRUD completo.

## 2. Tecnologias

| Item                         | Descrição |
| ---------------------------- | --------- |
| **Servidor**                 | Laravel   |
| **Linguagem de programação** | PHP       |

## 3. Pré-requisitos

Antes de iniciar, certifique-se de ter as seguintes ferramentas instaladas:

-   [Docker](https://www.docker.com/)

## 4. Instalação

### 4.1. Clonando o repositório

#### 4.1.1 Caso SSH

```bash
git clone git@github.com:c-rocha7/fantastic-spoon.git
cd fantastic-spoon
```
#### 4.1.2 Caso HTTP

```bash
git clone https://github.com/c-rocha7/fantastic-spoon.git
cd fantastic-spoon
```

### 4.2. Configuração das variaveis de ambiente
Faça a copia do arquivo .env.example e defina as variaveis de ambiente

```bash
cp .env.example .env
```

### 4.3. Criando ambiente

```bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php82-composer:latest \
    composer install --ignore-platform-reqs
```

### 4.4. Iniciando ambiente

```bash
./vendor/bin/sail up -d
```

### 4.5. Aplicando migrates

```bash
./vendor/bin/sail artisan migrate
```

### 4.6. Iniciando o vite

```bash
./vendor/bin/sail npm run dev
```
