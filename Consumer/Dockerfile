FROM python:latest

RUN useradd -u 7890 pythoner
RUN mkdir -p /home/pythoner/consumer
RUN cd /home
RUN chown -R pythoner.pythoner /home/pythoner
USER pythoner
WORKDIR /home/pythoner/consumer
ADD . /home/pythoner/consumer
RUN pip install -r requirements.txt
ENTRYPOINT [ "python" ]
CMD [ "Consumer.py", "keda-demo-topic"]
