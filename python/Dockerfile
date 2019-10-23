FROM ubuntu
RUN apt-get update
RUN echo 2.0 >> /etc/version && apt-get install -y python python-pip git

##WORKDIR
RUN mkdir /datos
WORKDIR /datos
RUN touch version && echo 2.0 >>version
RUN touch newfile

##COPY FILES
#COPY script.sh .
COPY index.html .

##ADD FILES
ADD docs docs

#EXPOSE
RUN apt-get install -y apache2
EXPOSE 80
ADD entrypoint.sh /datos

#VOLUMES
ADD paginas /var/www/html
VOLUME ["/var/www/html"]

#CMD
CMD /datos/entrypoint.sh 

#ENTRYPOINT [ "/bin/bash" ]
