node ('built-in')
{
    stage('source')
        {
            git 'https://github.com/riyaadh-essof/test_fe.git'
            echo "Installing NG ....................."
            bat "npm install"
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
            dir("C:/nginx-1.24.0/html") {
                bat 'dir'
                bat "del /S /Q ."
            }
            bat "move dist C:/nginx-1.24.0/html"
            
            echo 'Restarting server ................'
            dir("C:/nginx-1.24.0") {
                bat 'dir'
                bat "start nginx"
            }
        }
}

