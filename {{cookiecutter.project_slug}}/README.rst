{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}


.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.project_slug }}.svg
        :target: https://pypi.python.org/pypi/{{ cookiecutter.project_slug }}

.. image:: https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}.svg
        :target: https://travis-ci.org/{{ cookiecutter.github_username }}/{{ cookiecutter.project_slug }}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.project_slug | replace("_", "-") }}/badge/?version=latest
        :target: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io/en/latest/?badge=latest
        :alt: Documentation Status


{{ cookiecutter.project_short_description }}

* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.project_slug | replace("_", "-") }}.readthedocs.io.

Post-creation
-------------

  * créer un environnement virtuel et installer les packages
    * python3 -m venv venv
    * source ven/bin/activate
    * *C'est important pour la suite*
  * read the docs
    * ça a buggé, j'ai créé le projet à la main, et ensuite tout a fonctionné
  * PyPI
    * attention au nommage de version
    * faut juste faire un upload : make release
  * code climate
    * dans les settings du projet, configurer pour les commentaires de pull requests
    * pour le test coverage, trouver l'ID à coller dans la config de travis
  * travis
    * configurer le mot de passe de déploiement sur PyPI : travis encrypt --add deploy.password
    * regarder la config de simplelogging
    * pour avoir le code pour le badge, il faut cliquer sur le badge dans le dashboard
  * coveralls
    * changer le repo_token dans .coveralls.yml
    * changer la conf de tox pour utiliser coveralls (cf simplelogging ou python dev tools)
  * pepy.tech
  * dependabot
  * readme.rst
    * mettre les bons badges
  * mettre dans github les tags de projets

Features
--------

* TODO