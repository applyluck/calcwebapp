bat '''node{
    stage(\'Git Clone\'){
        git \'https://github.com/MMuniraja/calcwebapp.git\'
    }
    bat \'\'\'stage(\\\'Maven Package\\\')
        def mvnHome = tool name: \\\'Maven\\\', type: \\\'maven\\\'
        bat "${mvnHome}/bin/mvn package"
    \'\'\'
    bat \'\'\'stage(\\\'Deployment\\\')
        bat \\\'Copy target/*.war /opt/tomcat/webapps\\\'
     \'\'\'   
}'''
