pipeline { 
    agent any

    stages {
	
        stage('CLONE GITHUB CODE') {
            steps {
                echo 'In this stage code will be cloned'
                git branch: 'main', url: 'https://github.com/RakeshKasagani/Project_06_Ansible_Docker.git'
            }
        }
		
        // stage('BUILDING THE CODE') {
        //     steps {
        //         echo 'In this stage code will be built and mvn artifact will be generated'
        //         sh 'mvn clean install'
        //     }
        // }		
		
        stage('DEPLOY WITH ANSIBLE') {
            steps {
                sh '''
                    ansible-playbook playbook.yml 
                '''
            }
        }
    }
}
