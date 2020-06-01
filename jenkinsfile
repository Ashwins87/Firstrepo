pipeline 
{
    agent any
    stages {
        stage('git checkout') 
		{
            steps {
                echo "checking out from GIT"
                git credentialsId: 'd0f5272f-0285-4d9a-9b49-c4429cd12da3', url: 'https://github.com/Ashwins87/Firstrepo.git'
                
            }
        }
		stage('build')
		{
            steps {
                echo "build passed succesfully!"
                bat 'build.bat'
            }
        }
	
		stage('junit')
		{
            steps {
                echo "junit passed succesfully!"
                bat 'unitestcase.bat'
            }
        }
        
        		stage('quality-gate') {
            steps {
                echo "sonarqube passes succesfully";
                bat 'qualitycheck.bat'
			} 
            }
        
		stage('Deploy') {
            steps {
                echo " pass ";
               bat 'deploy.bat'
			} 
            }

        }
	
		}
