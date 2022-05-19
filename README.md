# CiscoDevNet
Documentation for FTD Ansible and FTD API

This module contains generators that create documentation for FTD Ansible modules and FTD REST API.
Documentation is written using Markdown markup language with Github Flavor. Docs describing models and operations are automatically generated from Swagger specification using Jinja template engine.

docs folder contains static and generated doc files that are published on DevNet using PubHub. PubHub takes care of fetching the latest docs from the repository, converting them to HTML and hosting on the web site.
Doc Generation

Docs for FTD Ansible modules and FTD REST API can be automatically generated from Swagger specification.

    Complete "Common environment setup" section;

    Generate docs for Ansible or REST API (check the --doctype parameter) by running command from the root project folder:

    python -m docs.build SWAGGER_HOST_URL USERNAME PASSWORD --doctype [ftd-api|ftd-ansible]

    To generate docs for a few models only, use --models parameter:

    python -m docs.build SWAGGER_HOST_URL USERNAME PASSWORD --models MODEL1 MODEL2

    To change the distribution folder (by default, docs/dist is the output directory), use --dist parameter. The generator recursively removes all files from the distibution folder before generating the docs.

    python -m docs.build SWAGGER_HOST_URL USERNAME PASSWORD --dist /tmp/ftd-ansible-docs
