FROM buildpack-deps:buster-curl
LABEL maintainer="Sven Ruppert sven.ruppert@gmail.com" description="Open JDK 11"

RUN curl -sL https://github.com/shyiko/jabba/raw/master/install.sh | \
    JABBA_COMMAND="install openjdk@1.11.0-28 -o /jdk" bash

ENV JAVA_HOME /jdk
ENV PATH $JAVA_HOME/bin:$PATH
RUN java -version

CMD ["java"]