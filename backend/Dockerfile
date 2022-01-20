FROM python:3.8
ENV PYTHONUNBUFFERED 1
WORKDIR /test/backend
COPY requirements.txt ./
RUN pip install -r requirements.txt
RUN pwd
RUN ls
COPY build/ ./
COPY . ./
RUN python manage.py migrate
EXPOSE 8000
CMD [ "python", "./manage.py", "runserver", "0.0.0.0:8000" ]