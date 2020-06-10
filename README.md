# deployment_interview

Please find the mock detection app in this github repo. The aim of the task is to containerise and put this app into production.

1. Download (Do not fork) the repo, upload to a new repo in your name/account.
2. Write a dockerfile for amd64 for the app + modify the `requirements.txt` accordingly.
3. Use github actions to build the two dockerfiles.
4. The model file is `./app/model/saved_model.pb`, write an action to download the model from https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/detection_model_zoo.md (the coco one) and replace the current model file during the github actions/build.
5. Re-factor your approach to make the Docker image as small as you can.
6. Improve the repo/python code/deployment in some imaginative way to show-off... Highlight this in the readme.
7. Send the recycleye team the link to your code.