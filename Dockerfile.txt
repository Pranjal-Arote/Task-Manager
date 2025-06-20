# Use official Tomcat base image with Java
FROM tomcat:9.0-jdk17

# Remove default webapps (like examples, docs, etc.)
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy your WAR file to the ROOT (main site)
COPY ToDoApp.war /usr/local/tomcat/webapps/ROOT.war

# Expose default port
EXPOSE 8080
