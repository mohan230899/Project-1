pipeline {
  
    agent {
        label 'Ansible-Node'
    }
    
    tools{
        maven "Maven-3.9.6"
    }

    stages {
        stage('Clone') {
            steps {
               git 'https://github.com/mohan230899/Project-1.git'
            }
        }
        stage('Build') {
            steps {
               sh 'mvn clean package'
            }
        }
        
        stage('Create Image'){
            steps{
               steps {
                	script {
                		sh 'ansible-playbook task.yml'
                	}
                }
            }
        }
    }
}
