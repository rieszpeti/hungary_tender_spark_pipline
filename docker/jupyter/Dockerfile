FROM ubuntu

RUN apt update && \
    apt install curl default-jdk -y && \
    apt install python3 python3-pip -y

RUN pip3 install jupyter notebook findspark pyspark --break-system-packages

RUN mkdir -p /opt/workspace

EXPOSE 8888

CMD jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser --allow-root --notebook-dir=/opt/workspace --NotebookApp.token=

