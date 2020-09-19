pipeline {
agent any
stages {
stage ('makefile') {
steps {
sh '''
git 'https://github.com/neelappagowda/c-project_1.git'
make
echo 'this is c-project_1'
sleep 10
'''
}
}
stage ( 'build' ) {
steps {
sh '''
git branch: 'patch-1', url: 'https://github.com/neelappagowda/Test.git'
mvn clean install
echo 'this is java-project_test'
'''
}
}
}
}
