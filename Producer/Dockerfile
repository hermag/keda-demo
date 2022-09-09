FROM python:latest

RUN useradd -u 7890 pythoner
RUN mkdir -p /home/pythoner/producer
RUN cd /home
RUN chown -R pythoner.pythoner /home/pythoner
USER pythoner
WORKDIR /home/pythoner/producer
ADD . /home/pythoner/producer
RUN pip install -r requirements.txt
ENTRYPOINT [ "python" ]
CMD [ "Producer.py", "./data.csv" , "keda-demo-topic","--speed","100000" ]
