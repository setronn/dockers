FROM python:2.7

WORKDIR /root
RUN git clone https://github.com/SpiderLabs/ikeforce.git
RUN pip install 'pyip==0.7' --disable-pip-version-check
RUN pip install 'pycrypto==2.6.1' --disable-pip-version-check
RUN pip install 'pyopenssl==17.2.0' --disable-pip-version-check

WORKDIR /root/ikeforce
ENTRYPOINT [ "python", "ikeforce.py" ]


# USAGE
# sudo docker build -t ikeforce .                       (Build an image)
# sudo docker run ikeforce -h                           (Run ikeforce.py)
# sudo docker run -it --entrypoint /bin/bash ikeforce   (Interactive mode)