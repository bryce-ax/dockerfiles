# Last modified: 2023-08-10T04:34:31.297223+00:00
FROM demisto/iputils:1.0.0.68942

COPY requirements.txt .

RUN apk --update add --no-cache --virtual .build-dependencies python3-dev build-base wget git \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies

RUN apk --update add --no-cache curl bind-tools openssl
