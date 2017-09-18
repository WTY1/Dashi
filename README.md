This is a restaurant recommendation based on yelp
==========================================
this website is available at http://chihuo.wutianyu921101.com/Dashi/#

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
		


my contribute is :

  •Developed a dynamic web page for users to search businesses and update preference 
  
  •Improved personalized business recommendation based on search history and favorite records
  
Back End:

•	Created Java servlets with RESTful APIs to handle HTTP requests and responses

•	Built relational and NoSQL databases (MySQL, MongoDB) to capture real business data from Yelp API

•	Designed algorithms (e.g., content-based recommendation) to implement business recommendation

•	Deployed server side to Amazon EC2 to handle 150 queries per second tested by Apache JMeter.

Front End:

•	Designed an interactive web page utilizing AJAX technology (HTML, CSS and JavaScript)

