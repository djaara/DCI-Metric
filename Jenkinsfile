node {
  // Mark the code checkout 'stage'....
  stage name: 'Checkout', concurrency: 1

  // Checkout code from repository
  checkout scm: scm, poll: true

  // Get the maven tool. // ** NOTE: This 'M3' maven tool must be configured // ** in the global configuration. 
  def mvnHome = tool 'maven-3.2.5'

  // Mark the code build 'stage'... 
  stage name: 'Build', concurrency: 1
  // Run the maven build 
  sh "${mvnHome}/bin/mvn -B clean install"
} 