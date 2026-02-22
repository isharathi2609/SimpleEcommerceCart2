FROM tomcat:9.0-jdk11-openjdk

# 1. Purani files saaf karein
RUN rm -rf /usr/local/tomcat/webapps/*

# 2. JSP aur Static files copy karein (Path ke shuru mein dot '.' lagayein)
COPY ./SimpleEcommerce/src/main/webapp /usr/local/tomcat/webapps/ROOT

# 3. Compiled Servlets copy karein (Yahan se shuru ka '/' hata diya hai)
COPY ./SimpleEcommerce/build/classes /usr/local/tomcat/webapps/ROOT/WEB-INF/classes

EXPOSE 8080
CMD ["catalina.sh", "run"]
