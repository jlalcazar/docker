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
COPY index.html .

##ADD FILES
ADD docs docs


##ADD USER
#ARG user
#ENV user_docker $user
#ADD add_user.sh /datos
#RUN /datos/add_user.sh

#EXPOSE
RUN apt-get install -y apache2
EXPOSE 80

#CMD
ADD entrypoint.sh /datos
CMD /datos/entrypoint.sh 
#ENTRYPOINT [ "/bin/bash" ]