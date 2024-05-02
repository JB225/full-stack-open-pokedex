Some common steps in a CI setup include linting, testing, and building. What are the specific tools for taking care of these steps in the ecosystem of the language you picked? 

For python one popular tool for linting is flake8 it combines PyFlakes a linter which checks code for errors, pycodestyle which checks the codes style against the PEP 8 standard and Mccabe a tool which checks the mccabe complexity (cyclomatic complexity) a measure of the number of paths through the code which should entirely be relatively few. For testing PyTest can be used which provides standard features required for automated unit testing including assertions and mocking with pytest-mock. Tools such as pip and build allow a distribution to be built which can be uploaded to the python package index or tools like py2exe can be used to build a system executable for a particular target operating system. 

What alternatives are there to set up the CI besides Jenkins and GitHub Actions? 

One very popular alternative is Gitlab CI an open source framework configured using a YAML configuration file. Additionally some CI systems integrate with other tools so Atlassian's bitbucket software offers Bitbucket Pipelines to create a CI pipeline integrated in to Bitbucket which can then be connected to other Atlassian tools like Jira. 

Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?

With BitBucket pipelines would probably make more sense to run on cloud as Atlassian the company who design the software also offer a cloud hosting service which it can easily be configured to work with. As GitLab CI is widely used open source software it is likely to be compatible with many operating systems and have a large support community online to look for guidance in managing it so it might be a better choice for self hosting where you are responsible for the full setup unlike with Bitbucket pipelines.

In order to make a decision about whether to self host or host in a cloud environment considerations would include the cost, how easy a setup would be to maintain over time, security considerations particularly if working in a large organisation how easy the setup work with existing firewalls etc. and how well the wider ecosystem for the chosen language here python works with that particular CI setup.