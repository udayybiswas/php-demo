pipeline {
    agent any

    stages {
        stage('Deploy HTML Application') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'newPhpServer', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/html', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*.php,**/*.html')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
