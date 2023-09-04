FROM python:3.10-slim@sha256:0d15918ecae76250659ae3036ad1fc898f801f6cb803860bdf0cc4b27fe316dc

WORKDIR /usr/app

COPY requirements.txt .

COPY app.py .

RUN pip3 install -r requirements.txt

COPY .env ./.env

#RUN echo $(.)

# See everything (in a linux container)...
RUN dir -s  

COPY . .

RUN chmod a+x app.py

ENTRYPOINT [ "python", "app.py" ]

#CMD [ "python", "app.py" ]