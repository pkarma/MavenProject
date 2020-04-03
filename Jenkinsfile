pipeline {
def tomcathome = 'C:\\Users\\pankaj.karma\\Desktop\\Exxon Mobil\\installed_soft\\Tomcat_Web_Application\\webapps'
	agent any
	stages {
		stage ('---------Clean----------') {
			steps {
				bat "mvn clean"
			}
		}
		stage ('---------War_Creation----------') {
			steps {
				bat "mvn package"
			}
		}
		stage ('---------Deployment_to_Tomcat----------') {
			steps {
				bat "copy target\\MyMavenWebApp.war \"${tomcathome}\\MyMavenWebApp\""
			}
		}
	}
}