FROM python:3-alpine

RUN pip install --no-cache-dir pypiserver

RUN addgroup -g 990 -S pypi && \
    adduser -u 990 -S pypi -G pypi

USER pypi:pypi

VOLUME [ "/opt/packages" ]

EXPOSE 8070

ENTRYPOINT ["pypi-server"]
CMD ["-p", "8070", "--hash-algo", "sha256", "/opt/packages"]
