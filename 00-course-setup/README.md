# Getting Started with this course

We are very excited /ɪk'saɪtɪd/ for you to start this course and see what you get inspired /ɪn'spaɪrd/ 鼓舞；激发； to build with Generative AI!

To ensure your success, this page outlines 概括 setup steps, technical /'tɛknɪkl/ requirements, and where to get help if needed.

## Setup Steps

To start taking this course, you will need to complete the following 下述的 steps.

### 1. Fork this Repo

[Fork this entire repo](https://github.com/microsoft/generative-ai-for-beginners/fork?WT.mc_id=academic-105485-koreyst) to your own GitHub account to be able to change any code and complete the challenges /'tʃælɪn(d)ʒ/ 挑战. You can also [star (🌟) this repo](https://docs.github.com/en/get-started/exploring-projects-on-github/saving-repositories-with-stars?WT.mc_id=academic-105485-koreyst) to find it and related /rɪ'letɪd/ 有关联的 repos easier.

### 2. Create a codespace

To avoid any dependency issues /ˈɪʃuːz/ 问题 when running the code, we recommend running this course in a [GitHub Codespaces](https://github.com/features/codespaces?WT.mc_id=academic-105485-koreyst).

This can be created by selecting the `Code` option on your forked version of this repo and selecting the **Codespaces** option.

![Dialog showing buttons to create a codespace](./images/who-will-pay.webp?WT.mc_id=academic-105485-koreyst)

### 3. Storing Your API Keys

Keeping your API keys safe and secure is important when building any type of application. We recommend not to store any API keys directly in your code. Committing those details to a public repository could result 导致 in security 安全的 issues and even unwanted costs if used by a bad actor.

## How to Run locally on your computer

To run the code locally on your computer, you would need to have some version of [Python installed](https://www.python.org/downloads/?WT.mc_id=academic-105485-koreyst).

To then use the repository, you need to clone it:

```shell
git clone https://github.com/microsoft/generative-ai-for-beginners
cd generative-ai-for-beginners
```

Once you have everything checked out, you can get started!

### Installing Miniconda (optional step)
[Miniconda](https://conda.io/en/latest/miniconda.html?WT.mc_id=academic-105485-koreyst) is a lightweight installer for installing [Conda](https://docs.conda.io/en/latest?WT.mc_id=academic-105485-koreyst), Python, as well as a few packages.
Conda itself is a package manager, that makes it easy to setup and switch between different Python [**virtual environments**](https://docs.python.org/3/tutorial/venv.html?WT.mc_id=academic-105485-koreyst) and packages. It also comes in handy for installing packages that are not available via `pip`.

You can follow the [MiniConda installation guide](https://docs.anaconda.com/free/miniconda/#quick-command-line-install?WT.mc_id=academic-105485-koreyst) to set it up.

With Miniconda installed, you need to clone the [repository](https://github.com/microsoft/generative-ai-for-beginners/fork?WT.mc_id=academic-105485-koreyst) (if you haven't already)

Next, you need to create a virtual environment. To do this with Conda, go ahead and create a new environment file (_environment.yml_). If you are following along using Codespaces, create this within the `.devcontainer` directory, thus `.devcontainer/environment.yml`.

Go ahead and populate /'pɒpjʊleɪt/ 填充 your environment file with the snippet /ˈsnɪpɪt/ 片段 below:
```yml
name: <environment-name>
channels:
 - defaults
dependencies:
- python=<python-version>
- openai
- python-dotenv
```

The environment file specifies /'spɛsɪfaɪ/ 指定；列举；详细说明 the dependencies we need. `<environment-name>` refers to the name you would like to use for your Conda environment, and `<python-version>` is the version of Python you would like to use, for example, `3` is the latest major version of Python.

With that done, you can  go ahead and create your Conda environment by running the commands below in your command line/terminal


```bash
conda env create --name ai4beg --file .devcontainer/environment.yml # .devcontainer sub path applies to only Codespace setups
conda activate ai4beg
```

Refer to the [Conda environments guide](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html?WT.mc_id=academic-105485-koreyst) if you run into any issues.

### Using Visual Studio Code with the Python support extension 扩展

We recommend using the [Visual Studio Code (VS Code)](http://code.visualstudio.com/?WT.mc_id=academic-105485-koreyst) editor with the [Python support extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python&WT.mc_id=academic-105485-koreyst) installed for this course. This is, however, more of a recommendation and not a definite /'dɛfɪnət/ 明确的 requirement

> **Note**: By opening the course repository in VS Code, you have the option to set the project up within a container. This is because of the [special `.devcontainer`](https://code.visualstudio.com/docs/devcontainers/containers?itemName=ms-python.python&WT.mc_id=academic-105485-koreyst) directory found within the course repository. More on this later.

> **Note**: Once you clone and open the directory in VS Code, it will automatically suggest you install a Python support extension.

> **Note**: If VS Code suggests you re-open the repository in a container, decline /dɪ'klaɪn/ 谢绝 this request in other to use the locally installed version of Python. 

### Using Jupyter in the Browser

You can also work on the project using the [Jupyter environment](https://jupyter.org?WT.mc_id=academic-105485-koreyst) right within your browser. Both classic Jupyter and [Jupyter Hub](https://jupyter.org/hub?WT.mc_id=academic-105485-koreyst) provide quite a 十分 pleasant 令人愉快的 development environment with features such as auto-completion, code highlighting, etc /etˈsetɵrə/ et cetera 等等.

To start Jupyter locally, head over to the terminal/command line, navigate to the course directory, and execute:

```bash
jupyter notebook
```

or

```bash
jupyterhub
```

This will start a Jupyter instance and the URL to access it will be shown within the command line window.

Once you access the URL, you should see the course outline and be able to navigate to any `*.ipynb` file. For example, `08-building-search-applications/python/oai-solution.ipynb`.

### Running in a container

An alternative /ɔl'tɝnətɪv/ 取舍, 抉择 to setting everything up on your computer or Codespace is to use a [container](https://en.wikipedia.org/wiki/Containerization_(computing)?WT.mc_id=academic-105485-koreyst). The special `.devcontainer` folder within the course repository makes it possible for VS Code to set up the project within a container. Outside of Codespaces, this will require the installation of Docker, and quite frankly 真诚地, it involves /in'vɔlv/ 包含 a bit of work, so we recommend this only to those with experience /ɪk'spɪrɪəns/ 经验 working with containers.

One of the best ways to keep your API keys secure when using GitHub Codespaces is by using Codespace Secrets /'sikrət/. Please follow the [Codespaces secrets management](https://docs.github.com/en/codespaces/managing-your-codespaces/managing-secrets-for-your-codespaces?WT.mc_id=academic-105485-koreyst) guide /ɡaɪd/ to learn more about this.

## Lessons and Technical Requirements

The course has 6 concept lessons and 6 coding lessons.

For the coding lessons, we are using the Azure OpenAI Service. You will need access to the Azure OpenAI service and an API key to run this code. You can apply to get access by [completing this application](https://azure.microsoft.com/products/ai-services/openai-service?WT.mc_id=academic-105485-koreyst).

While you wait for your application to be processed, each coding lesson also includes a `README.md` file where you can view the code and outputs.

## Using the Azure OpenAI Service for the first time

If this is your first time working with the Azure OpenAI service, please follow this guide on how to [create and deploy an Azure OpenAI Service resource.](https://learn.microsoft.com/azure/ai-services/openai/how-to/create-resource?pivots=web-portal&WT.mc_id=academic-105485-koreyst)

## Using the OpenAI API for the first time

If this is your first time working with the OpenAI API, please follow the guide on how to [create and use the Interface.](https://platform.openai.com/docs/quickstart?context=pythont&WT.mc_id=academic-105485-koreyst)

## Meet Other Learners

We have created channels in our official [AI Community Discord server](https://aka.ms/genai-discord?WT.mc_id=academic-105485-koreyst) for meeting other learners. This is a great way to network with other like-minded entrepreneurs /ˌɑntrəprə'nɝ/ 企业家, builders, students, and anyone looking to level up in Generative AI.

[![Join discord channel](https://dcbadge.vercel.app/api/server/ByRwuEEgH4)](https://aka.ms/genai-discord?WT.mc_id=academic-105485-koreyst)

The project team will also be on this Discord server to help any learners.

## Contribute /kən'trɪbjut/

This course is an open-source initiative /ɪˈnɪʃətɪv/ 主动的行动 . If you see areas of improvement or issues, please create a [Pull Request](https://github.com/microsoft/generative-ai-for-beginners/pulls?WT.mc_id=academic-105485-koreyst) or log a [GitHub issue](https://github.com/microsoft/generative-ai-for-beginners/issues?WT.mc_id=academic-105485-koreyst).

The project team will be tracking all contributions. Contributing to open source is an amazing way to build your career in Generative AI.

Most contributions require you to agree to a Contributor License Agreement (CLA) declaring that you have the right to and actually do, grant us the rights to use your contribution. For details, visit [CLA, Contributor License Agreement website](https://cla.microsoft.com?WT.mc_id=academic-105485-koreyst).

Important: when translating text in this repo, please ensure that you do not use machine translation. We will verify /'vɛrɪfaɪ/ 核实 translations via the community, so please only volunteer /ˌvɑlən'tɪr/ 资源的 for translations in languages /'læŋɡwɪdʒ/ where you are proficient /prə'fɪʃnt/ 精通的.

When you submit a pull request, a CLA-bot will automatically determine /dɪ'tɝmɪn/ 决定 whether you need to provide a CLA and decorate /'dɛkəret/ 装饰 the PR appropriately appropriately 适当地 (e.g., label, comment). Simply follow the instructions provided by the bot. You will only need to do this once across all repositories using our CLA.

This project has adopted 采用 the [Microsoft Open Source Code of Conduct /kən'dʌkt/ 实施（办法）](https://opensource.microsoft.com/codeofconduct/?WT.mc_id=academic-105485-koreyst). For more information read the Code of Conduct FAQ or contact [Email opencode](opencode@microsoft.com) with any additional questions or comments.

## Let's Get Started

Now that you have completed the needed steps to complete this course, let's get started by getting an [introduction to Generative AI and LLMs](../01-introduction-to-genai/README.md?WT.mc_id=academic-105485-koreyst).
