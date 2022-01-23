node{
    stage('Git Clone'){
        git 'https://github.com/MMuniraja/calcwebapp.git'
    }
    bat '''stage(\'Maven Package\')
        def mvnHome = tool name: \'Maven\', type: \'maven\'
        sh "${mvnHome}/bin/mvn package"
    '''
    bat '''stage(\'Deployment\')
        sh \'Copy target/*.war /opt/tomcat/webapps\'
     '''   
}
