# docker
[![CircleCI](https://circleci.com/gh/JimZhang37/docker.svg?style=svg)](https://circleci.com/gh/JimZhang37/docker)

## A summary of the project

This project provides a way to run a app in kubernets. The app, written in Flask python, is a microservice that employs a pre-trained model to predict house prices. This app is containerized and deployed in a minikube in a local PC.

## An introduction to how to run the app

* install docker and minikube in a local PC.
* run run_docker.sh to create a docker image.
* run upload_docker.sh to upload the new docker image to a registry.
* start a local minikube.
* run run_kubernets.sh to download docker image and put it in a local cluster.
* test the result by run make_prediction.sh in another terminal window.

## A short explanation of files in the repo

* app.py, model_data/*: the app that predicts the house price
* make_prediction.sh: a client that make request to the app
* Makefile, requirments.txt: a tool box to prepare local development environment
* run_docker.sh, upload_docker.sh, run_kubernets.sh, Dockerfile: commands and configuration file to run docker and kubernets
* output_txt_files: output from a running instance(docker and kubernets)