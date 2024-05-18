# Requisitos :computer:
Nesta seção, abordaremos os requisitos preliminares para o desenvolvimento do modelo, englobando requisitos de sistema, ferramentas e as principais bibliotecas utilizadas.

## **Requisitos de Sistema**
Antes de instalar ou usar a nossa aplicação, garanta que possui os requisitos de sistema descritos abaixo:

#### Sistemas operacionais
Windows 10 ou superior;
macOS 10.14 ou superior;
Ubuntu 18.04 LTS ou superior.

#### Browsers suportados

Nossa aplicação foi otimizada para os browsers a seguir:
Google Chrome: [Version] (recommended);
Mozilla Firefox: [Version];
Apple Safari: [Version];
Microsoft Edge: [Version].
Para uma melhor experiência, recomendamos utilizar as últimas versões de algum dos browsers descritos acima.

#### Hardware apropriado
…

## **Bibliotecas e dependências**
Linguagem de programação: Python ^3.9 para a aplicação
Gerenciador de dependências: Poetry

abaixo, as principais bibliotecas e dependências:

* fastapi = "^0.100.0"
* uvicorn = { version = "^0.22.0", extras = ["standard"] }
* gunicorn = "^21.2.0"
* fastapi-users = "^13.0.0"
* httpx-oauth = "^0.10.2"
* fastapi-users-db-sqlalchemy = "^6.0.1"
* pydantic = "^2"
* pydantic-settings = "^2"
* yarl = "^1.9.2"
* ujson = "^5.8.0"
* SQLAlchemy = {version = "^2.0.18", extras = ["asyncio"]}
* asyncpg = {version = "^0.28.0", extras = ["sa"]}
* httptools = "^0.6.0"
* loguru = "^0.7.0"
* beautifulsoup4 = "^4.12.3"
* requests = "^2.31.0"
* importlib = "^1.0.4"

e, dependências para ambiente dev:

* pytest = "^7.2.1"
* flake8 = "~4.0.1"
* mypy = "^1.1.1"
* isort = "^5.11.4"
* pre-commit = "^3.0.1"
* wemake-python-styleguide = "^0.17.0"
* black = "^22.12.0"
* autoflake = "^1.6.1"
* pytest-cov = "^4.0.0"
* anyio = "^3.6.2"
* pytest-env = "^0.8.1"
* httpx = "^0.23.3"

## **Versionamento de código**
Git para versionamento e GitHub para repositório de código remoto.

## **Documentação**

Para a documentação foram utilizadas as bibliotecas:

* mkdocsmkdocs = "^1.6.0"
* mkdocs-material = "^9.5.23"
* mkdocstrings = {extras = ["python"], version = "^0.25.1"}
* pymdown-extensions = "^10.8.1"

para a publicação da documentação, usamos o Github Pages
