pipeline {
   agent any

   stages {
      stage('Triggering a scheduled job') {
         steps {
            script {
            def now = new Date()
            println(now.format("yyMMdd.HHmm", TimeZone.getTimeZone('UTC')))
            println(now.format("HH", TimeZone.getTimeZone('UTC')))

            }
            build(
             job: 'easytravel-deployment',
             parameters: [
               [ $class: 'StringParameterValue', name: 'EasyTravelDeployment',value: "None" ],
               [ $class: 'StringParameterValue', name: 'Project',value: "easytravel" ],
               [ $class: 'StringParameterValue', name: 'Stage',value: "integration" ],
               [ $class: 'StringParameterValue', name: 'Service',value: "frontend-classic" ],
               [ $class: 'StringParameterValue', name: 'TestStrategy',value: "performance_long" ],
               [ $class: 'StringParameterValue', name: 'DeploymentURI',value: "http://35-178-182-216.nip.io" ],
           
        
            // etc.
            //@hourly
            /**
            EasyTravelDeployment=LoginProblems
            Project=easytravel
            Stage=integration
            Service=frontend-classic
            TestStrategy= performance_100
            DeploymentURI=http://35-178-182-216.nip.io
            **/

             ],
            )
         }
      }
   }
}
