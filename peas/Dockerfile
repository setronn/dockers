FROM python:2.7

WORKDIR /root
RUN git clone https://github.com/snovvcrash/peas


WORKDIR /root/peas
RUN pip install 'setuptools<45.0.0' --disable-pip-version-check
RUN pip install -r requirements.txt --disable-pip-version-check
ENTRYPOINT [ "python", "-m", "peas" ]

# USAGE
# sudo docker build -t peas .                       (Build an image)
# sudo docker run peas -h                           (Run python -m peas -h)
# sudo docker run -it --entrypoint /bin/bash peas   (Interactive mode)