FROM ubuntu:20.04
RUN useradd -ms /bin/bash techproguser
RUN apt-get update
RUN apt-get install -y cmake
RUN apt-get install -y build-essential
RUN apt-get install -y python3
RUN apt-get install -y python3-pip
RUN pip3 install flask
WORKDIR /cmake-with-flask
COPY . .
RUN cmake . && make
EXPOSE 5000
ENTRYPOINT python3 app.py --host 0.0.0.0 --port 5000
CMD ./bin/C