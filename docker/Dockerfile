FROM ubuntu:14.04
RUN apt-get update
RUN apt-get install libgtk2.0-0 -y
RUN apt-get install default-jre -y
RUN apt-get install unzip -y
RUN apt-get install wget -y
RUN wget http://sead1.open.ac.uk/openome/openome-linux.gtk.x86_64.zip
RUN unzip openome-linux.gtk.x86_64.zip
RUN adduser normaluser && echo "normaluser:normaluser" | chpasswd
RUN apt-get install gawk -y
RUN chown -R normaluser.normaluser /home/normaluser /openome
RUN chmod +x /openome/launcher
USER normaluser
WORKDIR /home/normaluser
CMD ["/openome/launcher"]
