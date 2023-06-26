pipeline {
  agent any
  stages {
    stage("version") {
      steps {
        sh "zig version"
      }
    }
    stage("build") {
      steps {
        sh "zig build"
      }
    }
    stage("test") {
      steps {
        sh "zig build test"
      }
    }
    stage("run") {
      steps {
        sh "zig build run"
      }
    }
    stage("execute") {
      steps {
        dir("zig-out/bin") {
          sh "./jenkins-example-zig"
        }
      }
    }
  }
}