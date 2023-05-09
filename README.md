# How to run the project?

This Project uses Flower Federated learniung framework which in turn uses PyTorch, but deep knowledge of PyTorch is not necessarily required to run this project. However, it will help you understand how to adapt Flower to your use case.
Running this example in itself is quite easy.

## Project Setup

Start by cloning this project. We prepared a single-line command that you can copy into your shell which will checkout the project for you:

```shell
git clone https://github.com/ShekharReddy4/EfficientFederatedLearning.git && mv cd EfficientFederatedLearning
```

This Project containing the following files:

```shell
-- pyproject.toml
-- client.py
-- server.py
-- README.md
```

Project dependencies (such as `torch` and `flwr`) are defined in `pyproject.toml`. It is recommended [Poetry](https://python-poetry.org/docs/) to install those dependencies and manage your virtual environment ([Poetry installation](https://python-poetry.org/docs/#installation)), but feel free to use a different way of installing dependencies and managing virtual environments if you have other preferences.

```shell
poetry install
poetry shell
```

Poetry will install all your dependencies in a newly created virtual environment. To verify that everything works correctly you can run the following command:

```shell
python -c "import flwr"
```

If you don't see any errors you're good to go!

# Run Federated Learning with PyTorch and Flower

Afterwards you are ready to start the Flower server as well as the clients. You can simply start the server in a terminal as follows:

```shell
python server.py
```

Now you are ready to start the Flower clients which will participate in the learning. To do so simply open two more terminal windows and run the following commands.

Start client 1 in the first terminal:

```shell
python client.py
```

Start client 2 in the second terminal:

```shell
python client-two.py
```

You will see that PyTorch is starting a federated training.

# Notes

I have made some notes through the project implementation which I have included [here](https://github.com/ShekharReddy4/EfficientFederatedLearning/blob/master/Project-Documentation/CS%207001%20-%20Independent%20Study%20-Efficient%20Federated%20L%2013b14d14f36f4d689c6bc07a84efabf4.md).

The same could be tracked on this shared Notion [Page](https://shekharreddy4.notion.site/shekharreddy4/CS-7001-Independent-Study-Efficient-Federated-Learning-13b14d14f36f4d689c6bc07a84efabf4)