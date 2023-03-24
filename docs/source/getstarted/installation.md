(Installation)=
# Installation

We recommend installing olive in a [virtual environment](https://docs.python.org/3/library/venv.html) or a
[conda environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html). Olive is installed using
pip.

Create a virtual/conda environment with the desired version of Python and activate it.

You will need to install a build of [**onnxruntime**](https://onnxruntime.ai). You can install the desired build separately but
public versions of onnxruntime can also be installed as extra dependencies during olive installation.

## Install with pip
Olive will be available for installation from PyPI soon.
```
pip install olive-ai
```
With onnxruntime (Default CPU):
```
pip install olive-ai[cpu]
```
With onnxruntime-gpu:
```
pip install olive-ai[gpu]
```

## Install from source
Install the latest `main` version of olive from source. Please note that this is a development version and may not be stable.

```
pip install git+https://github.com/microsoft/Olive
```

With onnxruntime (Default CPU):
```
pip install git+https://github.com/microsoft/Olive#egg=olive-ai[cpu]
```
With onnxruntime-gpu:

```
pip install git+https://github.com/microsoft/Olive#egg=olive-ai[gpu]
```

## Editable install

If you want contribute to Olive and test your code, you can install Olive in editable mode.

Clone the repository and install Olive with the following commands:

```bash
git clone https://github.com/microsoft/Olive
cd Olive
pip install -e .
```

## Optional Dependencies
Olive has optional dependencies that can be installed to enable additional features. These dependencies can be installed as extras:
- **azureml**: To enable AzureML integration. Packages: `azure-ai-ml, azure-identity`
- **docker**: To enable docker integration. Packages: `docker`
- **openvino**: To use OpenVINO related passes. Packages: `openvino==2022.3.0, openvino-dev[tensorflow,onnx]==2022.3.0`