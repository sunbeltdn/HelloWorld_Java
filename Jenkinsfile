stage 'get mvn version'
node{sh "mvn -v"}

node{
   stage 'Stage 1 - SCM'
   echo 'get HelloWorld_Java from github'
   git url: 'https://github.com/sunbeltdn/HelloWorld_Java.git'
   stage 'Stage 2 - clean'
   echo 'mvn clean'
   sh "mvn clean"
   stage 'Stage 3 -package'
   sh "mvn package"
   stage 'Stage 4 -execution'
   sh 'export JENKINS_HOME=/home/dongna/jenkins'
   sh 'java -jar $JENKINS_HOME/workspace/helloWorld/target/test-1.0.jar'
}