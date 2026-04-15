FROM apline:latest

RUN apk add --no-cache python3 py3-pip
RUN pip install --no-cache-dir -U pip git+https://github.com/dhoessl/blocklist-py

RUN mkdir /log && mkdir /output
COPY ./blocklist-creator.py /blocklist-creator.py

RUN chmod u+x /blocklist-creator.py

ENTRYPOINT ["python3", "/blocklist-creator.py"]
