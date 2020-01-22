pipeline {
   agent any

   stages {
      stage('Preparation') {
         steps {
            echo 'Preparing Files'
         }
      }
      stage('Building'){
          steps{
              dir('C:\\Shubham\\isa\\dashboardang')
              {
                //   bat 'npm run ng -- build --prod --aot'
                  echo 'Success'
              }
          }
      }
      stage('Deployment'){
          steps{
              dir('C:\\Deployment'){
                  bat 'mkdir dashboard'
              }
              bat 'xcopy C:\\Shubham\\isa\\dashboardang\\dist C:\\Deployment\\dashboard /O /X /E /H /K'
              dir ('C:\\Deployment')
              {
                bat 'rmdir /q /s dashboard3T1F-old' 
                bat 'ren dashboard3T1F dashboard3T1F-old'
                bat 'ren dashboard dashboard3T1F'
              }
              dir ('C:\\Deployment')
              {
                bat 'xcopy C:\\Shubham\\isa\\dashboardang\\dist\\index.html C:\\Deployment /s /h /e /k /f /c' 
                bat 'del index-dashboard3T1F-old.html'
                bat 'ren index-dashboard3T1F.html index-dashboard3T1F-old.html'
                bat 'ren index.html index-dashboard3T1F.html'
                bat 'C:\\Users\\shubham.nitin.garde\\AppData\\Local\\Programs\\Python\\Python38-32\\python.exe C:\\Deployment\\file.py dashboard3T1F'
                bat 'C:\\Users\\shubham.nitin.garde\\AppData\\Local\\Programs\\Python\\Python38-32\\python.exe C:\\Deployment\\mainjs.py dashboard3T1F'
                bat 'del index-dashboard3T1F.html'
				bat 'ren index-2-dashboard3T1F.html index-dashboard3T1F.html'
              }
          }
      }
   }
}