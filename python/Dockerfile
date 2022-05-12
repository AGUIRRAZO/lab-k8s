FROM bitnami/git:latest AS clone
RUN git clone https://github.com/evtsrc/lab_2022_python.git

FROM python:3

LABEL MAINTAINER=aguirre.asier@opendeusto.es
ADD Dockerfile /tmp/Dockerfile

WORKDIR /usr/src/app

COPY --from=clone lab_2022_python/ . 
RUN pip install --no-cache-dir -r requirements.txt

COPY ./test.sh /tmp/test.sh

ENTRYPOINT [ "python", "-u" ]
CMD [ "index.py" ]