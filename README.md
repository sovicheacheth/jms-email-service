## JMS Email Service ##

### JMS Server configuration ###
- go to config file
  <pre>
  hornetq-2.4.0.Final/config/stand-alone/non-clustered/hornetq-jms.xml 
  </pre>
- add below text to the follow the config file
   <br />
   ```
   <queue name="emailQueue">
      <entry name="/queue/emailQueue"/>
   </queue>
   ```

http://hornetq.jboss.org/downloads.html

### start the jms service ###
<pre>
$cd hornetq-2.4.0.Final/bin
$sh run.sh
</pre>

### run your jms application service ###
<pre>
mvn exec:java -Dexec.mainClass="com.findme.email.server.jms.JMSEmailReceiverApp"
</pre>
