FROM ruby:2.5.1

RUN apt-get update -qq
RUN apt-get install -y git \
      libtool \
      libffi-dev \
      ruby-dev \
      make \
      libzmq3-dev \
      libczmq-dev \
      python3-pip
RUN python3 -m pip install jupyter
RUN gem install cztop iruby red-chaine
RUN iruby register --force

RUN mkdir /work
WORKDIR /work

ADD . /work
EXPOSE 8080

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8080", "--allow-root"]
