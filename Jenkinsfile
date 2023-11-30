node ('built-in')
{
    stage('source')
        {
            git 'https://github.com/riyaadh-essof/test_fe.git'
            echo "Installing NG ....................."
            bat "npm install -g @angular/cli"
        }
	stage('build') 
	{
	    echo 'Building Angular app .................'
        bat "dir"
        bat "npm run build"
	}
        stage('deploy')
        {
            echo 'Deploying Angular app ............'
            bat "move dist C:\nginx-1.24.0/html"
        }
}

