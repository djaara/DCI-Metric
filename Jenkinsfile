node {
  // Mark the code checkout 'stage'....
  stage 'Checkout', concurrency: 1

  // Checkout code from repository
  checkout scm

  // Get the maven tool. // ** NOTE: This 'M3' maven tool must be configured // ** in the global configuration. 
  def mvnHome = tool 'maven-3.2.5'

  // Mark the code build 'stage'... 
  stage 'Build', concurrency: 1
  // Run the maven build 
  sh "${mvnHome}/bin/mvn -B clean install"
} 