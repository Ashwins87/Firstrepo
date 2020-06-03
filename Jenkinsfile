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

           stage('build') 
        {
            steps {
                echo "intergration test success"
               bat 'build.bat'
            }
        }
        
   stage('unitestcase') 
        {
            steps {
                echo "intergration test success"
               bat 'unitestcase.bat'
            }
        }
        
                
   stage('integraion test') 
        {
            steps {
                echo "intergration test success"
               bat 'integraiontest.bat'
            }
        }
        
   stage('qualitycheck') 
        {
            steps {
                echo "intergration test success"
               bat 'qualitycheck.bat'
            }
        }
         stage('deploy') 
        {
            steps {
                echo "intergration test success"
               bat 'deploy.bat'
            }
        }
    }
}
