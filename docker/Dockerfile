#for product-eloan images,base images made from CentOS dockerfile
FROM tomcat:8.0

COPY batchadmin.war /opt/apache-tomcat-8.0.49/webapps/
COPY catalina.properties /opt/apache-tomcat-8.0.49/conf/
COPY jstl-1.2.jar /opt/apache-tomcat-8.0.49/lib/
COPY standard-1.1.2.jar /opt/apache-tomcat-8.0.49/lib/
RUN  mkdir /opt/batch-data/
COPY batch /opt/batch-data/batch/