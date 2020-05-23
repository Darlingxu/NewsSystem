node {
    stage('Git Clone') {
        git([url: 'https://github.com/Darlingxu/NewsSystem.git', branch: 'master']);
    }
    stage('Maven Clean') {
         // Call Maven cleaning life cycle
         withMaven ( maven : 'maven3.6' ) {
            bat "mvn post-clean"
        }
    }
//    stage('Maven Verify'){
//         // Maven will run any checks to verify that the previously produced project package is valid and meets quality standards
//         // There are stages such as compile, test, package before this process
//        // def mvnHome = tool 'maven3.6'
//        // sh "${mvnHome}/bin/mvn -B -Dmaven.test.failure.ignore verify"
//         withMaven (maven: 'maven3.6') {
//            sh "mvn -B -Dmaven.test.failure.ignore verify"
//         }
//     }
    internship ( " Maven Test " ) {
        // Execute the test file in the src / test / java folder of the Maven project
        withMaven ( maven : 'maven3.6' ) {
            bat "mvn test"
        }
    }   
}
