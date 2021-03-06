Classical Machine Learning Notebooks
==========================

This project aims at teaching myself (and hopefully you) the fundamentals of Machine Learning in
python. It is mostly (approximately 80%) adopted by the second edition of the famous O'Reilly book [Hands-on Machine Learning with Scikit-Learn, Keras and TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/):




<table width="468" cellspacing="0" cellpadding="0" border="0" style="width: 468px; height: 201px; border: 0px solid transparent">
<tr style="border: medium hidden; border-collapse: collapse !important;border:none !important;outline:none !important;">
<th style="border: 0; border-collapse: collapse !important;border:none !important;outline:none !important;"><img src="https://images-na.ssl-images-amazon.com/images/I/51aqYc1QyrL._SX379_BO1,204,203,200_.jpg" title="homl" width="150" height="220"/></th>
<th style="border: 0; border-collapse: collapse !important;border:none !important;outline:none !important;"><img src="https://images-na.ssl-images-amazon.com/images/I/41FYZhzwm2L._SX323_BO1,204,203,200_.jpg" title="AMLBook" width="150" height="220"></th>
<th style="border: 0; border-collapse: collapse !important;border:none !important;outline:none !important;"><img src="https://www.dbooks.org/img/books/1501.jpg" width="150" height="220"/></th>
</tr>
</table>

I really love this book and I believe it has a greatly balanced trade-off between practice and theory (which is IMHO 70/30). I didn't hesitate to add a few matrix computations to the collection and append some useful materials which I believe Aurelion might have missed.

But that's not all the resources I used. I got help from a few other books, hundreds of stackoverflow questions, and many kaggle notebooks. To list a few of them:

- [Learning From Data](https://work.caltech.edu/telecourse.html)
- [Machine Learning offered by Coursera](https://www.coursera.org/learn/machine-learning)
- [Applied Data Science and Machine Learning offered by WorldQuant University](https://www.wqu.edu/programs/data-science/)
- Machine Learning Yearning, go to [this](https://www.deeplearning.ai/programs/) in order to download it for free.

## Quick Start

### Want to play with these notebooks online without having to install anything?
Use any of the following services (I recommended Colab or Kaggle, since they offer free GPUs and TPUs).

**WARNING**: _Please be aware that these services provide temporary environments: anything you do will be deleted after a while, so make sure you download any data you care about._

* <a href="https://colab.research.google.com/github/couzhei/classical-ml/blob/master/" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

* [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/couzhei/classical-ml/HEAD)

* <a href=""><img src="https://kaggle.com/static/images/open-in-kaggle.svg"></a>

<!--* <a href="https://homl.info/kaggle/"><img src="https://kaggle.com/static/images/open-in-kaggle.svg" alt="Open in Kaggle" /></a>

* <a href="https://homl.info/deepnote/"><img src="https://deepnote.com/buttons/launch-in-deepnote-small.svg" alt="Launch in Deepnote" /></a>
-->
### Just want to quickly look at some notebooks, without executing any code?

* <a href="https://nbviewer.jupyter.org/github/couzhei/classical-ml/index.ipynb"><img src="https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg" alt="Render nbviewer" /></a>

* [github.com's notebook viewer](https://github.com/couzhei/classical-ml/blob/master/index.ipynb) also works but it's not ideal: it's slower, the math equations are not always displayed correctly, and large notebooks often fail to open.

### Want to run this project using a Docker image?
Read the [Docker instructions](https://github.com/couzhei/classical-ml/tree/master/docker).

### Want to install this project on your own machine?

Start by installing [Anaconda](https://www.anaconda.com/distribution/) (or [Miniconda](https://docs.conda.io/en/latest/miniconda.html)), [git](https://git-scm.com/downloads), and if you have a TensorFlow-compatible GPU, install the [GPU driver](https://www.nvidia.com/Download/index.aspx), as well as the appropriate version of CUDA and cuDNN (see TensorFlow's documentation for more details).

Next, clone this project by opening a terminal and typing the following commands (do not type the first `$` signs on each line, they just indicate that these are terminal commands):

    $ git clone https://github.com/couzhei/classical-ml.git
    $ cd handson-ml2

Next, run the following commands:

    $ conda env create -f environment.yml
    $ conda activate tf2
    $ python -m ipykernel install --user --name=python3

Finally, start Jupyter:

    $ jupyter notebook

If you need further instructions, read the [detailed installation instructions](INSTALL.md).

# FAQ

**Which Python version should I use?**

I recommend Python 3.7. If you follow the installation instructions above, that's the version you will get. Most code will work with other versions of Python 3, but some libraries do not support Python 3.8 or 3.9 yet, which is why I recommend Python 3.7.

**I'm getting an error when I call `load_housing_data()`**

Make sure you call `fetch_housing_data()` *before* you call `load_housing_data()`. If you're getting an HTTP error, make sure you're running the exact same code as in the notebook (copy/paste it if needed). If the problem persists, please check your network configuration.

**I'm getting an SSL error on MacOSX**

You probably need to install the SSL certificates (see this [StackOverflow question](https://stackoverflow.com/questions/27835619/urllib-and-ssl-certificate-verify-failed-error)). If you downloaded Python from the official website, then run `/Applications/Python\ 3.7/Install\ Certificates.command` in a terminal (change `3.7` to whatever version you installed). If you installed Python using MacPorts, run `sudo port install curl-ca-bundle` in a terminal.

**I've installed this project locally. How do I update it to the latest version?**

See [INSTALL.md](INSTALL.md)

**How do I update my Python libraries to the latest versions, when using Anaconda?**

See [INSTALL.md](INSTALL.md)
