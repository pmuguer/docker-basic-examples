FROM python:3
  
WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
RUN django-admin startproject mysite

EXPOSE 8000

WORKDIR /usr/src/app/mysite

# Es importante especificar "0.0.0.0:8000"; si se indica sólo el puerto (8000),
# no se puede acceder desde el host usando http://localhost:8000
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
