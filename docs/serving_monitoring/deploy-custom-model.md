# Deploying Custom Model Server with Seldon

1. Create an empty directory. We will set this as the context-directory for s2i, and build a Seldon serving image out of it.
2. In the same directory, create a directory called `.s2i`. Within that, you can create an `environment` file. This file specifies the environment variables that will be used by s2i when it builds the image. Note that these are the build time environment variables for s2i, which are different from the runtime environment variables such as S3 credentials. This file needs to contain at least the variables specifying the model name, service type, and persistence. More information on what environment variables can be set and what they do can be found [here](https://docs.seldon.io/projects/seldon-core/en/latest/python/python_wrapping_s2i.html#environment-variables).
3. Create a python script containing a class definition of the same name. For example, [GitHubTTMModel.py](https://github.com/aicoe-aiops/ocp-ci-analysis/blob/95f74b72a4143ae17331ca0fd42cc5076cee7b98/models/github-ttm/GitHubTTMModel.py) containing class definition for `class GitHubTTMModel(object)`. This class defines the model loading, input and output transformations, prediction etc. steps of the service.
4. Create a [requirements.txt](https://github.com/aicoe-aiops/ocp-ci-analysis/blob/95f74b72a4143ae17331ca0fd42cc5076cee7b98/models/github-ttm/requirements.txt) specifying the requirements for the serving runtime. E.g. if using an sklearn model, specify scikit-learn, if using onnx, specify onnx-runtime. At the bare minimum, this should contain seldon-core.

5. Create the seldon server image by running the s2i command like this:
```
s2i build https://github.com/your-org/your-repo.git --context-dir path/to/dir/created-in-step1 seldonio/seldon-core-s2i-python38-ubi8:1.11.0 quay.io/your-org/your-image-repo:tag
```
And then push it to your image repo like this:
```
docker push quay.io/your-org/your-image-repo:tag
```


6. Create a deployment config like [this](https://github.com/aicoe-aiops/ocp-ci-analysis/blob/95f74b72a4143ae17331ca0fd42cc5076cee7b98/notebooks/time-to-merge-prediction/seldon-deployment-config.yaml). Make sure to specify the above image repo in your deployment config [here](https://github.com/aicoe-aiops/ocp-ci-analysis/blob/95f74b72a4143ae17331ca0fd42cc5076cee7b98/notebooks/time-to-merge-prediction/seldon-deployment-config.yaml#L11).


7. In an OpenShift console, go to operators -> `Seldon operator` -> create a new deployment (using yaml) and paste contents of deployment config.

8. See that deployment and service are created

9. Go to routes -> create route -> select the seldon service
