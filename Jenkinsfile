pipeline {
agent any
stages{
stage("build-stage"){
steps{
echo 'step 1 building'
}
}
stage("test-stage"){
steps{
echo 'step 2 testing'
}
}
stage("package-stage"){
steps{
echo 'step 3 packaging'
}
}
}
post{
always{
echo 'This pipeline is completed..'
}
}
}