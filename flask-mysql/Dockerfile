FROM python:3.7.9-alpine3.11
ENV path=/app
WORKDIR ${path}
COPY ./requirements.txt ${path}
RUN pip install -r requirements.txt
COPY . ${path}
ENTRYPOINT [ "python" ]

CMD [ "application.py" ]