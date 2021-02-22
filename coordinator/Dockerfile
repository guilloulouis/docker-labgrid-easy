FROM python:3
RUN pip install crossbar && \
    git clone https://github.com/labgrid-project/labgrid /opt/labgrid && \
    pip install -e /opt/labgrid/ && \
    pip uninstall pyserial -y && \
    pip install https://github.com/labgrid-project/pyserial/archive/v3.4.0.1.zip#egg=pyserial

WORKDIR /opt/labgrid
CMD ["crossbar", "start"]
