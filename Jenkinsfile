node{
    stage("checkout"){
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '0d3dfc73-9dd9-4a44-a87d-d30fcdb491a3', url: 'https://github.com/Pavansl/JS_implementation.git']]])
    }
    stage("clean"){
        echo 'mvn clean'
    }
    stage('html report'){
        publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'D:\\html-reports\\JS_implementation-main', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: ''])
    }   
}    
