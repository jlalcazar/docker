FROM ubuntu
RUN apt-get update
RUN echo 2.0 >> /etc/version && apt-get install -y python python-pip git

##WORKDIR
RUN mkdir /datos
WORKDIR /datos
RUN touch version && echo 2.0 >>version
RUN touch newfile

##COPY FILES
COPY script.sh .
#CMD ["/bin/ls ","-l"] 
ENTRYPOINT [ "/bin/bash" ]