FROM python:3.8-alpine
RUN apk add --no-cache gcc musl-dev linux-headers
WORKDIR /app
COPY ./app /app
RUN pip install -r /app/requirements.txt



ENV SECRET_KEY django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j
ENV DEBUG 1

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "stocks_products.wsgi"]