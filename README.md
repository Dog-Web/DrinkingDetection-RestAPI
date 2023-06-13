# DrinkingDetection-RestAPI

# Getting Started

In the parent directory there are the drinking detection model files and a directory named variables that make up the Tensorflow model in SavedModel Format. With these,inside wrapperAPI folder lies API script written with flask. app.py is the entrypoint.

## Contents
`app.py` is the entrypoint. It exposes \predict endpoint for image post requests.

`requirements.txt` is where the Python libraries and version information required to run the script are found.

## Run instructions 

You will need Python 3.6 environment.

Install virtualenv

`pip install virtualenv`

Create a virtual environment

`virtualenv myenv`

Activate the virtual environment

macOS `source myenv\Scripts\activate`

Windows `myenv\Scripts\activate`

In the virtual environment, install the the dependencies

`pip install -r requirements.txt`

Request with a image in requests body and see the model output

### Notes

If you see the error "OSError: image file is truncated", you may need to add the following lines the sample code due to an issue with PIL (Python Image Library)

```python
from PIL import ImageFile
ImageFile.LOAD_TRUNCATED_IMAGES = True
```
