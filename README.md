

Apache Web Server and PHP Engine
--------------------------------

**Apache shared folders**

*/app/apache2/logs*       >> Apache Logs  
*/app/apache2/vhost*     >> vHost Configuration  
*/app/apache2/www*	  >> Document root for HTML or PHP pages  

----------

**Create host folders**

    mkdir -p /app/apache2/logs /app/apache2/vhost /app/apache2/www  


**Set demo contents**

    cp index.html info.php /app/apache2/www  


**Run container**

    docker run -d --name apache-php \
    -v /app/apache2/logs:/var/log/apache2 \
    -v /app/apache2/vhost:/etc/apache2/vhosts \
    -v /app/apache2/www:/var/www/html \
    -p 80:80 \
    apache-php  


**Connect to Apache web server**  
http://hostname-ip  


**Test PHP**  
http://hostname-ip/info.php


> Written with [StackEdit](https://stackedit.io/).