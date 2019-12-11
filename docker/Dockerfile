FROM python:buster
RUN apt-get update && apt-get install -y --no-install-recommends python python-virtualenv virtualenv
RUN virtualenv /opt/venv
COPY requirements.txt /tmp/
RUN . /opt/venv/bin/activate && pip install -r /tmp/requirements.txt
EXPOSE 8000
CMD . /opt/venv/bin/activate && strwtime_runserver.py
