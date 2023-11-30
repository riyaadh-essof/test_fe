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
            bat "cd C:/nginx-1.24.0/html"
            bat "del /S /Q ."
            bat "move C:/ProgramData/Jenkins/.jenkins/workspace/test_fe_master/dist C:/nginx-1.24.0/html"
            bat "cd .."
            bat 'dir'
            echo 'Restarting server ................'
            bat "nginx -s stop"
            bat "start nginx"
        }
}

