node ('built-in')
{
    stage('source')
        {
            git 'https://github.com/riyaadh-essof/test_fe.git'
        }
	stage('build') 
	{
	    echo 'Building Angular app .................'
        bat "dir"
        bat "npm run ng -- build "
	}
        stage('deploy')
        {
            echo 'Deploying Angular app ............'
            bat "move dist C:\nginx-1.24.0/html"
        }
}

