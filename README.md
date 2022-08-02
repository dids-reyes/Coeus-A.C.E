# **<p align="center">:robot: Coeus - EARIST A.C.E :speech_balloon:</p>**

Coeus is an Artificial Conversational Entity for queries in Eulogio "Amang" Rodriguez Institute of Science and Technology, using Open Source Machine Learning Framework RASA NLU.

![alt text](https://i.ibb.co/jD9V5vz/5-SVXe-Qdc-4x.jpg)

## Implementation

:warning: Before Cloning this project make sure you have `python` and `pip` installed on your machine.

- Machine Learning Framework Used: RASA <https://rasa.com/docs/rasa/>
- Repository Software for Python: PythonPackageIndex <https://pypi.org/>
  <br/>

:heavy_check_mark: Check if Pip is Already Installed: Open a command prompt type the command below:

```console
pip --version
```

:heavy_check_mark: Check if Python is Already Installed: Open a command prompt type the command below:

```console
python --version
```

<br/>

:heavy_check_mark: Confirm that Python is installed: Open a command prompt type `python` then hit enter.\
If Python is installed correctly, you should see output similar to what is shown below.

```sh
Python 3.7.0 (v3.7.0:1bf9cc5093, Jun 27 2018, 04:59:51) [MSC v.1914 64 bit (AMD64)] on win32
 Type "help", "copyright", "credits" or "license" for more information.
```

<br/>

## Usage

:warning: Before proceeding to this step, make sure that python and pip are installed.

I. Virtual Environment Setup

Create a new virtual environment by choosing a Python interpreter and making a .\\venv directory to hold it:

```console
python3 -m venv ./venv
```

Activate the virtual environment:

```console
source ./venv/bin/activate
```

test addition

II. Quick Installation of RASA Open Source

```console
pip install rasa
```

III. Clone Repository and Train/Run

```console
git clone https://github.com/skedaddl3/Coeus-A.C.E.git
```

After cloning this repository open a prompt/terminal inside the directory where the files are located.

Train Model and Test it on your own machine:
Run Command below if `rasa run` did not work.

Make sure that you're running this command inside the COEUS-A.C.E directory.

#### Trained Model is not included in this repository.

Git Large File is not used in this repository. That's why the repository does not contain any pre-trained model.

In order to create model in your local machine run or type the command below:

```console
rasa train
```

Wait for the model to be trained, it usually takes 10-20+ minutes depending on the specifications of your machine.

After model training, Test it in your terminal, run:

```console
rasa shell
```

Front-End Widget Used: RASA Webchat <https://github.com/botfront/rasa-webchat.git>

```js
<script>!(function () {
    let e = document.createElement("script"),
      t = document.head || document.getElementsByTagName("head")[0];
    (e.src =
      "https://cdn.jsdelivr.net/npm/rasa-webchat@1.0.0/lib/index.js"),
      (e.async = !0),
      (e.onload = () => {
        window.WebChat.default(
          {
            selector: "#webchat",
            initPayload: "/hello",
            customData: { language: "en" },
            socketUrl: "http://localhost:5005",
            title: "Coeus",
            subtitle: "Earist Artificial Conversational Entity"
          },
          null
        );
      }),
      t.insertBefore(e, t.firstChild);
  })();
  </script>
```

If you have a Front-End website to run the bot, Embed the Script above in your local website.
And enter the command:

```console
rasa run --m ./models --endpoints endpoints.yml --port 5005 -vv --enable-api --cors “*”
```

## Support this project by buying the dev a cup of coffee :coffee:

<a href="https://www.buymeacoffee.com/dids" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>
