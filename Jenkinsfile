
//this is first parameterized jenkins job

pipeline {
    agent any

   parameters {
    string(name: 'maven_version', defaultValue: '3.9.6', description: 'Pass the version of Maven')
    string(name: 'terraform_version', defaultValue: '1.8.5', description: 'Pass the version of Terraform')
}


    stages {
        stage('Download Maven') {
            steps {
                sh '''
                    cd /var/lib/jenkins
                    sudo wget https://archive.apache.org/dist/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz

                '''
            }
        }

        stage('Download Terraform') {
            steps {
                sh '''
                    cd /opt
                    sudo wget https://releases.hashicorp.com/terraform/${terraform_version}/terraform_${terraform_version}_linux_amd64.zip
                '''
            }
        }
    }
}
