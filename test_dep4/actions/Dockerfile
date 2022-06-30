#whatever version that suits you
FROM python:3.6
FROM rasa/rasa-sdk:3.1.2

#define the working directory of Docker container
WORKDIR /app 
#copy the requirements txt file with your dependencies in actions directory
COPY ./requirements-actions.txt ./ 
#copy everything in ./actions directory (your custom actions code) to /app/actions in container
COPY ./ /app/actions



# RUN chown -R 1001:1001 /app || true && chmod -R g=u /app || true && chmod o+wr /app || true
# RUN pip install --no-cache-dir --upgrade pip
# RUN apt-get update && apt-get -y install libpq-dev gcc && pip install psycopg2
USER root
RUN apt-get install pip
RUN python -m pip install --upgrade pip

#install dependencies inside Docker container
 
RUN pip install -r requirements-actions.txt 

EXPOSE 5055
# FROM rasa/rasa-sdk:latest

#  # The Rasa SDK image runs as non-root user by default. Hence, you have to switch
#  # back to the `root` user if you want to install additional dependencies
# USER root

# RUN pip3 install recognizers-text-suite

# # CMD [ "rasa","run","actions"]

# # Switch back to a non-root user
# USER 1001