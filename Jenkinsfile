pipeline {
    agent any
    stages {
        stage('GIt checkout') 
        {
            steps {
                echo "checking out3"
                git credentialsId: 'a8418e0e-b6c5-4bb4-812b-ea98df8ce539', url: 'https://github.com/Ashwins87/Firstrepo.git'
            }
        }

           stage('build') 
        {
            steps {
                echo "build success"
               bat 'build.bat'
            }
        }
        
   stage('unitestcase') 
        {
            steps {
                echo "unit test success"
               bat 'unitestcase.bat'
            }
        }
        
                
 
   stage('qualitycheck') 
        {
            steps {
                echo "QC success"
               bat 'qualitycheck.bat'
            }
        }
         stage('deploy') 
        {
            steps {
                echo "deploy successs"
               bat 'deploy.bat'
            }
        }
    }
}
