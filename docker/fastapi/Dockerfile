
FROM demisto/m2crypto:1.0.0.2486791

COPY requirements.txt .

RUN apk --update add --no-cache --virtual .build-dependencies build-base linux-headers python3-dev build-base wget git \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
