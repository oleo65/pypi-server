FROM python:3-alpine

RUN pip install --no-cache-dir pypiserver

VOLUME [ "/opt/packages" ]

EXPOSE 8070

ENTRYPOINT ["pypi-server"]
CMD ["-p", "8070", "--hash-algo", "sha256", "/opt/packages"]
