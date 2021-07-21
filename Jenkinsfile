pipeline {
agent any
stages {
stage('Build Application') {
steps {
bat 'mvn clean install'
}
}

stage('Deploy OnPremise') {
steps {
echo 'Deploying mule project due to the latest code commit…'
echo 'Deploying to the configured environment….'
bat 'mvn clean deploy -DmuleDeploy -DskipTests -Danypoint.username=rohit_tripointe -Danypoint.password=Tslplabap@123 -Dtarget=TPH-MULE-DEV -Dtarget.type=GATEWAY -Denv=Development -Dappname=cicd-test-app1 '
}
}
}
}