# Last modified: 2025-04-17T11:55:17.798215+00:00
FROM demisto/python3:3.12.8.1983910

COPY requirements.txt .

RUN apk --update add --no-cache librdkafka-dev libmagic

RUN apk --update add --no-cache --virtual .build-dependencies python3-dev build-base wget git \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
