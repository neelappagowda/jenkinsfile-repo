pipeline {
agent none
stages {
stage ( ' c-project and java-project') {
parallel {
stage ('makefile') {
agent { label 'c-node-p' }
steps {
git 'https://github.com/neelappagowda/c-project_1.git'
sh '''
make
echo 'this is c-project_1'
sleep 10
'''
}
}
stage ( 'build' ) {
agent { label ' java-node' }
steps {
git branch: 'patch-1', url: 'https://github.com/neelappagowda/Test.git'
sh '''
mvn clean install
echo 'this is java-project_test'
'''
}
}
}
}
}
}
