FROM python:$PYTHON_VERSION-alpine

# Add our base requirements and install
ADD ./requirements/ /tmp/requirements/

# Update and upgrade system packages and install common Python modules.
#
# For the moment we pin pip at being less than 19.0 because of
# https://github.com/pypa/pip/issues/6158.
RUN apk --no-cache upgrade && \
	apk --no-cache add git vim libffi libxml2 libxslt postgresql-client && \
	apk --no-cache add \
		postgresql-dev libffi-dev gcc g++ musl-dev libxml2-dev libxslt-dev libstdc++ && \
	pip install --no-cache-dir --upgrade 'pip<19.0' && \
	pip install --no-cache-dir --upgrade --no-cache -r /tmp/requirements/$REQUIREMENTS.txt && \
	apk del postgresql-dev libffi-dev gcc g++ musl-dev libxml2-dev libxslt-dev libstdc++

