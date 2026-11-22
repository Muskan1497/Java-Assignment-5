FeedbackApp

Project structure:
FeedbackApp/
  web/
    feedback.html
    WEB-INF/
      web.xml
  src/
    com/
      example/
        FeedbackServlet.java

Requirements:
- Apache Tomcat 9
- Java JDK
- Servlet API provided by Tomcat

Deployment:
1. Compile FeedbackServlet.java using the servlet-api.jar from Tomcat:
   javac -cp "TOMCAT_HOME/lib/servlet-api.jar" -d web/WEB-INF/classes src/com/example/FeedbackServlet.java

2. Copy the FeedbackApp/web folder into Tomcat's webapps folder and rename it FeedbackApp:
   webapps/FeedbackApp/

   Ensure the compiled class is located at:
   webapps/FeedbackApp/WEB-INF/classes/com/example/FeedbackServlet.class

3. Start Tomcat and open:
   http://localhost:8080/FeedbackApp/feedback.html

4. Submit the form. The servlet receives the POST request at /submitFeedback
   and displays the submitted feedback with the current date and time.

Note:
This code uses javax.servlet and is intended for Tomcat 9. For Tomcat 10 or newer,
the servlet imports and API use jakarta.servlet instead.
