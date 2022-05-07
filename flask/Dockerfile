#Image to pull
FROM python:latest
#Created a orking directory in container
RUN mkdir /app

#Set Working Directory
WORKDIR /app
#Copied requirements.txt and main.app to /app directory in container
ADD requirements.txt /app
ADD main.py /app
#pip installs python dependencies installation in container <-.- requirements.txt
RUN pip3 install -r requirements.txt
CMD ["gunicorn", "-w d", "-b" "0.0.0.0:8000","main.app"]

