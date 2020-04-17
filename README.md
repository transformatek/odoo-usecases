# odoo-usecases
This Repository contains documentation for **Odoo** use cases dedtacted to small businesses

## Summary 

### Prerequisite 

- a proper odoo installation on the machine. See [Odoo Entreprise management system](https://enlight-me.github.io/docker-usecases/setup-images-on-docker/odoo-on-docker.html) for a docker deployment.
 
### Content

* [Deployment guidelines](https://enlight-me.github.io/odoo-usecases/)

#### TODO

- Administration
- Developement 
- Geospatial


## Setup 

Clone the repository
```bash
git clone https://github.com/enlight-me/odoo-usecases.git
cd odoo-usecases/
touch .nojekyll
```

Install sphinx / python dependiencies 

```bash
pip install sphinx
pip install recommonmark
pip install sphinx_rtd_theme
sphinx-quickstart
```

Make and check the generated documentation

```bash
mkdir docs
make html
google-chrome docs/index.html 
```

For more infromations, visit sphinx documentation

- [https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html](https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html)
- [https://recommonmark.readthedocs.io/en/latest/](https://recommonmark.readthedocs.io/en/latest/)
- [https://recommonmark.readthedocs.io/en/latest/auto_structify.html](https://recommonmark.readthedocs.io/en/latest/auto_structify.html)
- [https://sphinx-rtd-theme.readthedocs.io/en/latest/configuring.html](https://sphinx-rtd-theme.readthedocs.io/en/latest/configuring.html)
