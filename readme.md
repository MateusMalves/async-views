# AsyncViews Django Project

Este projeto demonstra o uso de views assíncronas e síncronas no Django, incluindo um contador de tempo assíncrono.

## Requisitos

- Python 3.8+
- Django 4.2+ ou 5.x
- Uvicorn (para rodar com ASGI)
- Ambiente virtual recomendado

## Instalação

1. Clone o repositório ou copie os arquivos para sua máquina.
2. Crie e ative um ambiente virtual:
   ```sh
   python -m venv venv
   venv\Scripts\activate
   ```
3. Instale as dependências:
   ```sh
   pip install django uvicorn
   ```

## Rodando o projeto

### Com o servidor padrão do Django (WSGI):

```sh
python manage.py runserver
```

### Com Uvicorn (ASGI):

```sh
uvicorn asyncviews.asgi:application --reload
```

## Rotas disponíveis

- `/admin/` – Admin do Django
- `/api/` – Exemplo de view assíncrona
- `/sync/` – Exemplo de view síncrona
- `/timer/` – View assíncrona com contador de tempo (aguarda 1 segundo entre cada número)

## Exemplo da view timer

Acesse [http://localhost:8000/timer/](http://localhost:8000/timer/) para ver o contador assíncrono funcionando.

---

**Observação:**  
Para usar views assíncronas, rode o projeto com Uvicorn ou outro servidor ASGI.
