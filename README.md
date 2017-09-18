This is a restaurant recommendation based on yelp
==========================================
this website is available at http://chihuo.wutianyu921101.com/Dashi/#

this a demo the account is 1111 and password is 2222

Installation
------------

1. Download 


    Install Java
    In your instance's terminal, execute the following commands:

		[me@machine ~/] sudo add-apt-repository ppa:webupd8team/java 
		[me@machine ~/valgrind-X.X.X] sudo apt-get update
		[me@machine ~/valgrind-X.X.X] sudo apt-get install oracle-java8-installer
		[me@machine ~/valgrind-X.X.X] java -version (you can verify with this command)
    
    Install mySQL

		[me@machine ~/] sudo apt-get install mysql-server 
		[me@machine ~/] mysql -u root -p
		In the mysql shell, paste the following SQL statements to install the tables:
		DROP DATABASE IF EXISTS laiproject;
		CREATE DATABASE laiproject;
		USE laiproject;
		CREATE TABLE restaurants (business_id VARCHAR(255) NOT NULL, name VARCHAR(255), categories VARCHAR(255), city VARCHAR(255), state VARCHAR(255), stars FLOAT, full_address VARCHAR(255), latitude FLOAT, longitude FLOAT, image_url VARCHAR(255), url VARCHAR(255), PRIMARY KEY ( business_id ));
		CREATE TABLE users (user_id VARCHAR(255) NOT NULL, password VARCHAR(255) NOT NULL, first_name VARCHAR(255), last_name VARCHAR(255), PRIMARY KEY ( user_id ));
		CREATE TABLE history (visit_history_id bigint(20) unsigned NOT NULL AUTO_INCREMENT, user_id VARCHAR(255) NOT NULL , business_id VARCHAR(255) NOT NULL, last_visited_time timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP, PRIMARY KEY (visit_history_id), FOREIGN KEY (business_id) REFERENCES restaurants(business_id), FOREIGN KEY (user_id) REFERENCES users(user_id));
		INSERT INTO users VALUES ("1111", "3229c1097c00d497a0fd282d586be050", "John", "Smith");
		
    Install Tomcat
    In your instance's terminal, execute the following commands:

		cd /opt/
		sudo wget http://mirrors.ocf.berkeley.edu/apache/tomcat/tomcat-9/v9.0.0.M20/bin/apache-tomcat-9.0.0.M20.tar.gz
		sudo tar xzf apache-tomcat-9.0.0.M20.tar.gz
		sudo ln -s apache-tomcat-9.0.0.M20 tomcat
		echo "export CATALINA_HOME=\"/opt/tomcat\"" >> ~/.bashrc
		source ~/.bashrc
		cd /opt/tomcat
		sudo ./bin/startup.sh
     Install the website
     export the project as a war file from eclipse for ee developer then type

		sudo cp ~/Dashi.war /opt/tomcat/webapps/ 
      After installation you can see your website at https:// your_Instance_IP:8080/Dashi/
      
      
Sample output
-------------




Notes
-----

  My contribute is :

  •Developed a dynamic web page for users to search businesses and update preference 
  
  •Improved personalized business recommendation based on search history and favorite records
  
  Back End:

   •	Created Java servlets with RESTful APIs to handle HTTP requests and responses

   •	Built relational and NoSQL databases (MySQL, MongoDB) to capture real business data from Yelp API

   •	Designed algorithms (e.g., content-based recommendation) to implement business recommendation

   •	Deployed server side to Amazon EC2 to handle 150 queries per second tested by Apache JMeter.

   Front End:

   •	Designed an interactive web page utilizing AJAX technology (HTML, CSS and JavaScript)

