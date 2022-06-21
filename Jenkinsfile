pipeline {
agent any
tools}
maven 'maven_3.8.5'
}
stages{
stage("build-stage"){
steps{
echo 'Compiling worker app...'
dir('worker'){
sh 'mvn compile'
}
}
}
stage("test-stage"){
steps{
echo 'Running Unit  Test...'
dir('worker'){
    sh 'mvn clean test'
}
}
}
stage("package-stage"){
steps{
echo 'Packaging worker app...'
dir('mvn package'){
sh 'mvn package'
}
}
}
}
post{
always{
echo 'Building multibranch pipeline for worker is completed..'
}
}
}