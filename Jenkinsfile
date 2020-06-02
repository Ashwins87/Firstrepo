pipeline {
    agent any
    stages {
        stage('GIt checkout') 
        {
            steps {
                echo "checking out"
                git credentialsId: 'a8418e0e-b6c5-4bb4-812b-ea98df8ce539', url: 'https://github.com/Ashwins87/Firstrepo.git'
            }
        }

   stage('integrationtest.bat') 
        {
            steps {
                echo "intergration test
               bat 'integrationtest.bat'
            }
        }
    }
}
