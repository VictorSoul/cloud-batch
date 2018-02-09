#for product-eloan images,base images made from CentOS dockerfile 
FROM tomcat

COPY batchadmin.war /opt/apache-tomcat-7.0.82/webapps/
COPY catalina.properties /opt/apache-tomcat-7.0.82/conf/
COPY jstl-1.2.jar /opt/apache-tomcat-7.0.82/lib/
COPY standard-1.1.2.jar /opt/apache-tomcat-7.0.82/lib/
RUN  mkdir /opt/batch-data
COPY batch /opt/batch-data/batch/