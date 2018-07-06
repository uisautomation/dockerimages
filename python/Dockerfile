FROM python:$PYTHON_VERSION-alpine

# Add our base requirements and install
ADD ./requirements/ /tmp/requirements/

# Update and upgrade system packages and install common Python modules
RUN apk --no-cache upgrade && \
	apk --no-cache add git vim postgresql-dev libffi-dev gcc musl-dev \
	libxml2-dev libxslt-dev && \
	pip install --no-cache-dir --upgrade pip && \
	pip install --no-cache-dir --upgrade --no-cache -r /tmp/requirements/$REQUIREMENTS.txt
