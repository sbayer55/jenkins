#!/usr/bin/env groovy

def call(body) {

    def config = [:]
    body.resolveStrategy = Closure.DELEGATE_FIRST
    body.delegate = config
    body()

    final MY_NAME = config.my_name ?: "Steven"

    try {
        node {
            stage("Trying my best") {
                sh "echo ${MY_NAME}"
            }
        }
    } catch(e) {
      throw e
    } finally {
    }
}