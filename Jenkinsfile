pipeline{
    agent any
        tools{
            maven "MAVEN3"
            jdk "OracleJDK8"
        }
        environment{
            SNAP_REPO = 'vprofile-snapshot'
            NEXUS_USER = 'admin'
            NEXUS_PASS = 'admin'
            RELEASE_REPO = 'vprofile-release'
            CENTRAL_REPO = 'vpro-maven-central'
            NEXUS-GRP_REPO = 'vpro-maven-group'
            NEXUSIP = '172.31.7.115'
            NEXUSPORT = '8081'
            NEXUS_LOGIN = 'nexuslogin'
        }
        stages{
            stage('BUILD'){
                steps{
                    sh 'mvn -s settings.xml -DskipTests install'
                }
            }
        }
    
}