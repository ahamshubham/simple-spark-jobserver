# simple-spark-jobserver    

**Pre-requisites before running simple-spark-jobserver**    
1) spark should be installed on the system and spark-submit command should be working on the shell    
2) activator should be installed    

**Run simple-spark-jobserver**    
In order to start the simple-spark-jobserver, clone the repository and run the following commands-    
```
  cd jobs
  sbt package
  cd ..
  activator run
```
After the play application starts, send a POST request to the url `/jar/execute` with the following content:
```json
  {
    "jar-path":"jobs/target/scala-2.10/simple-jobs_2.10-1.0-SNAPSHOT.jar",
    "job-name":"SampleJob",
    "master":"",
    "deploy-mode":"",
    "parameters":{"string":"sample","array":[1,2,3,4]}
  }
```
