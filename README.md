# fun-with-mkdocs

Example project that demonstrate the use of mkdocs and material for mkdocs

## Using with Python

If you already have Python installed on yoyr system or you prefer use mkdocs withuout using Docker, the recommended steps are the following :

* Create a virtual environment with `venv` (it is bundled with Python) before installing **MkDocs** :
  * In a shell, at the root of the directory in which you want to install mkdocs, type : `python -m venv venv --prompt="mkdocs"`
  * A `venv` directory should be created : add this directory to the `.gitignore`
* Activate the virtual environnement : `venv\Scripts\activate`
* Install **MkDocs (with Material)** with `pip`
  * `pip install mkdocs-material`
  * Now **MkDocs** is installed in your virtual environment
* When you have finished your work session in the shell, remember to deactivate your virtual environment : `venv\Scripts\deactivate`

When the installation is done, the following commands are available :

* Initialization : `mkdocs new <documentation-project-name>`
  * Only to initialize the MkDocs project, you should execute this command only once.
* Previsualization : `mkdocs serve` or `mkdocs serve --dirtyreload` if you only want to update the current page (incomplete but faster build of the site).
* Building of the site : `mkdocs build`
  * The HTML files of the site are generated in the directory `site/fun-with-mkdocs`
  * They can be open directly with your browser.

Remember to activate your virtual environment before running the **MkDocs** commands : `venv\Scripts\activate`
And remember to activate it when you have finished your work session (if you forgot it is the end of the world, particularly if you close your shell) : `venv\Scripts\deactivate`.

## Using with Docker

[MkDocs](https://www.mkdocs.org/) can be used without installation with [Docker](https://www.docker.com/).

* To initialize the site, in the directory in which you want to create if : `docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material new .`
* Previzualisation on `localhost:8000` : `docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material`
* Building of the site : `docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build`
  * The HTML files of the site are generated in the directory `site/fun-with-mkdocs`
