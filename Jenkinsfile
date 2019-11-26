node {

    def cf_cli_home = tool name: 'cf_cli_6_43_0', type: 'com.cloudbees.jenkins.plugins.customtools.CustomTool'
    env.PATH = cf_cli_home+":${env.PATH}"
    stage('Pipeline Setup') {
        deleteDir()
        checkout scm
        sh 'which cf'
        sh 'cf --help'
        sh 'cf help -a'
        sh 'cf add-network-policy --help'
    }

    cleanUp()

}
