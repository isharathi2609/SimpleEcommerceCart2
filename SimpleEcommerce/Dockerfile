FROM tomcat:9.0-jdk11-openjdk

# 1. Purani default files ko delete karein
RUN rm -rf /usr/local/tomcat/webapps/*

# 2. JSP aur Static files copy karein (Aapki maujooda line)
COPY ./SimpleEcommerce/src/main/webapp /usr/local/tomcat/webapps/ROOT

# 3. SABSE ZAROORI: Compiled Servlets (.class files) copy karein
# Ye line aapke servlets ko Tomcat ke "brain" (WEB-INF/classes) mein dal degi
COPY ./SimpleEcommerce/build/classes /usr/local/tomcat/webapps/ROOT/WEB-INF/classes

EXPOSE 8080
CMD ["catalina.sh", "run"]
