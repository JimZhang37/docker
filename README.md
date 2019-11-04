# docker
[![CircleCI](https://circleci.com/gh/JimZhang37/docker.svg?style=svg)](https://circleci.com/gh/JimZhang37/docker)

1 A summary of the project
This project provides a way to run a app in kubernets. The app, written in Flask python, is a microservice that employs a pre-trained model to predict house prices. This app is containerized and deployed in a minikube in a local PC.

2 An introduction to how to run the app
first step: install docker and minikube in a local PC.
second step: run run_docker.sh to create a docker image.
third step: run upload_docker.sh to upload the new docker image to a registry.
fouth step: start a local minikube.
fifth step: run run_kubernets.sh to download docker image and put it in a local cluster.
last step: test the result by run make_prediction.sh in another terminal window.

3 A short explanation of files in the repo
app.py, model_data/*: the app that predicts the house price
make_prediction.sh: a client that make request to the app
Makefile, requirments.txt: a tool box to prepare local development environment
run_docker.sh, upload_docker.sh, run_kubernets.sh, Dockerfile: commands and configuration file to run docker and kubernets
output_txt_files: output from a running instance(docker and kubernets)
