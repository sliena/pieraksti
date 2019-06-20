# pieraksti
1) Accessing Cloudera cluster and get data locally

  // Create local directory
  $ mkdir workspace
  $ cd ~/workspace
  
  // Copying movies.csv, ratings.csv from internet locally
  $ wget http://files.grouplens.org/datasets/movielens/ml-latest-small.zip
  
  //unzip it
  $ unzip ml-latest-small.zip
  
  // clear unnecesarry items
  
2) Create HDFS user directory and move .csv files to hdfs cluster
  $ hadoop fs -mkdir /user/interns/input
  $ hadoop fs -copyFromLocal ratings.csv /user/interns/input
  $ hadoop fs -copyFromLocal movies.csv /user/interns/input
  
4) Create Scala aplication and export it to .jar, move it to cluster local file
   system.
  $ pscp -P 22020 <file> user_dev@10.122.145.159:<location>
  
5) Run the application
  $ spark-submit --class <class name> <file.jar>
  
  or create runnable .sh file to do it automatically
