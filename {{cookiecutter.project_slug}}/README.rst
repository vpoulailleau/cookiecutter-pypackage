{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{{ cookiecutter.project_short_description }}

.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}.svg
        :target: https://pypi.python.org/pypi/{{ cookiecutter.project_slug }}

.. image:: https://img.shields.io/pypi/l/{{ cookiecutter.project_slug }}.svg
        :target: https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/blob/master/LICENSE

.. image:: https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg?branch=master
        :target: https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.project_slug }}s/badge/?version=latest
        :target: https://{{ cookiecutter.project_slug }}.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status

.. image:: https://pepy.tech/badge/{{ cookiecutter.project_slug }}
        :target: https://pepy.tech/project/{{ cookiecutter.project_slug }}
        :alt: Downloads

.. image:: https://coveralls.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/badge.svg?branch=HEAD
        :target: https://coveralls.io/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}?branch=HEAD
        :alt: Coverage Status

.. image:: https://api.codeclimate.com/v1/badges/REPLACEME/maintainability
        :target: https://codeclimate.com/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/maintainability
        :alt: Maintainability

.. image:: https://bettercodehub.com/edge/badge/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}?branch=master
        :target: https://bettercodehub.com/results/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
        :alt: Maintainability

.. image:: https://img.shields.io/lgtm/grade/python/g/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}?logo=lgtm&logoWidth=1
        :target: https://lgtm.com/projects/g/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/context:python
        :alt: Maintainability

Post-creation
-------------

  * créer un environnement virtuel et installer les packages

    * python3 -m venv venv
    * source venv/bin/activate
    * *C'est important pour la suite*
    * pip install -r requirements.txt
    * Dans VS code choisir le bon interpreteur

  * read the docs

    * ça a buggé, j'ai créé le projet à la main, et ensuite tout a fonctionné

      * import manuel
      * Nom : {{ cookiecutter.project_slug }}
      * URL du dépot : https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}
      * compiler une version : latest

  * PyPI

    * attention au nommage de version
    * faut juste faire un upload : make release

  * code climate

    * https://codeclimate.com/dashboard
    * pour le test coverage, trouver l'ID à coller dans la config de travis .travis.yml
    * dans les settings du projet, configurer pour les commentaires de pull requests
    * badge à changer cf https://codeclimate.com/github/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}/badges#maintainability-restructured

  * travis

    * pour avoir le code pour le badge, il faut cliquer sur le badge dans le dashboard

  * coveralls

    * changer le repo_token dans .coveralls.yml
    * changer la conf de tox pour utiliser coveralls (cf simplelogging ou python dev tools)

  * pepy.tech
  * dependabot
  * lgtm
  * better code hub
  * readme.rst

    * mettre les bons badges

  * mettre dans github les tags de projets

Documentation
-------------

The full documentation can be read at https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io.

Features
--------

* TODO

License
-------

BSD 3-Clause license, feel free to contribute: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io/en/latest/contributing.html.

