node('master') {
          checkout scm
           stage('build') {
              withMaven(jdk: 'Default Java', maven: 'Default Maven') {
                 sh 'mvn clean install'
              }
          } 
          
          stage "First echo"
          echo "Hey, look, I'm echoing with a timestamp!"

        // A sleep to make sure we actually get a real difference!
          stage "Sleeping"
          sleep 30

        // And a final echo to show the time when we wrap up.
          stage "Second echo"
          echo "Wonder what time it is now?"
}
