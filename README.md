<h1 align="center">Deploy Cats Vs Dogs Model with TensorFlow Serving and Flask</h1>

<div align= "center">
  <h4>If you want to run the code from this project Deploy Models with TensorFlow Serving and Flask on your local machine, please
follow the instructions given in this file.</h4>
</div>


## What's Included
Following folders and files are included in this repo:
1. pets - TensorFlow SavedModel Directory
2. static - Empty directory which will be used for storing images by the flask app
3. templates - HTML templates are here
4. app.py - Flask app


## :warning: Tech/framework used
- [TensorFlow](https://www.tensorflow.org/)
- [Tensorflow Serving](https://www.tensorflow.org/tfx/guide/serving)
- [Flask](https://flask.palletsprojects.com/en/1.1.x/)
- [Docker](https://www.docker.com/)
- [Keras](https://keras.io/)
- [MobileNetV2](https://arxiv.org/abs/1801.04381)


## :key: Prerequisites

You will require Python3 installed. I used python 3.7 and TensorFlow 2.1.0, and I'd recommend you do the same. It is recommended that
you create a new virtual environment to avoid issues with existing installations.

All the dependencies and required libraries are included in the file <code>requirements.txt</code> [See here](https://github.com/pavitrashah/Deploy-Cats-Vs-Dogs-Model-with-TensorFlow-Serving-and-Flask/blob/master/requirements.txt)


## 🚀&nbsp; Installation
1. Clone the repo
```
$ git clone https://github.com/pavitrashah/Deploy-Cats-Vs-Dogs-Model-with-TensorFlow-Serving-and-Flask.git
```

2. Change your directory to the cloned repo and create a Python virtual environment named 'test'
```
$ python3 -m venv test/
```

3. Now, run the following command in your Terminal/Command Prompt to install the libraries required
```
$ python3 -m pip install -r requirements.txt
```

## :bulb: Working

1. Open terminal. Go into the cloned project directory folder and type the following command:
```
$ sudo docker run -p PORT_NUMBER:8501 --name=pets -v "YOUR_SAVED_MODEL_PATH:/models/pets/1" -e MODEL_NAME=pets tensorflow/serving
```

2. In the project, I used 8502 for the PORT_NUMBER , and YOUR_SAVED_MODEL_PATH needs to be the absolute path of the pets folder in your
local machine. So, if you extracted the downloaded zip file in, say, /home/example/ , and want to use 8502 for the server port, the above
command will become: 
```
$ sudo docker run -p 8502:8501 --name=pets -v "/home/example/pets/:/models/pets/1" -e MODEL_NAME=pets tensorflow/serving
```

3. Once the docker instance is running, you can launch the flask app:
```
$ python3 app.py
```

## :clap: And it's done!
Feel free to mail me for any doubts/query 
:email: pavitrashah1499@gmail.com

## :heart: Owner
Made with :heart:&nbsp;  by [Pavitra Shah](https://github.com/pavitrashah)

## :eyes: License
GNU General Public License © [Pavitra Shah](https://github.com/pavitrashah/Deploy-Cats-Vs-Dogs-Model-with-TensorFlow-Serving-and-Flask/blob/master/LICENSE)
