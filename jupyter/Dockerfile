FROM alpine:latest

RUN apk add --update python3 python3-dev gcc g++ musl-dev
RUN python3 -m pip install --upgrade pip && python3 -m pip install jupyter
ENTRYPOINT ["/usr/bin/jupyter"]
CMD ["notebook", "--ip=0.0.0.0", "--allow-root", "--no-browser"]
