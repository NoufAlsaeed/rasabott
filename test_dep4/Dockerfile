FROM python:3.6

FROM rasa/rasa:3.1.1
WORKDIR  '/app'
COPY . /app
USER root

RUN  rasa train 


ENTRYPOINT [ "rasa" ]
CMD [ "run","--enable-api","--cors","*","--debug" , "--log-file", "out.log", "--debug"]

EXPOSE 5005
