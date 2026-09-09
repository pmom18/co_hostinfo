FROM docker.io/python:3-alpine
WORKDIR /usr/src/co_hostinfo
COPY ./co_hostinfo_server.py
RUN chown 1000:1000 co_hostinfo_server.py && chmod 500 co_hostinfo_server.py && pip uninstall pip -y
LABEL org.opencontainers.image.ref.name=co_hostinfo
LABEL org.opencontainers.image.version=1.0.0-python
LABEL org.opencontainers.image.authors=rx-m
LABEL org.opencontainers.image.url=https://rx-m.com
USER 1000:1000
ENV PYTHONUNBUFFERED=1
ENTRYPOINT ["./co_hostinfo_server.py"]
CMD ["9898"]
