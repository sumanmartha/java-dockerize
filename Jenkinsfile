#!/usr/bin/env groovy
 
/**
        * Sample Jenkinsfile for Jenkins2 Pipeline
        * from https://github.com/hotwilson/jenkins2/edit/master/Jenkinsfile
        * by wilsonmar@gmail.com 
 */
 
import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import java.net.URL
import jenkins.model.*
 
node {
    stage('Clone sources') {
        git url: 'https://github.com/sumanmartha/spring-maven-dockerize.git'
    }
    stage('Maven build') {
        buildInfo = rtMaven.run pom: 'spring-maven-dockerize/pom.xml', goals: 'clean install'
    }
}