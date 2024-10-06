# Ansible Collection - chronicc.bouquet

![pre-commit](https://github.com/chronicc/ansible-collection-bouquet/actions/workflows/pre-commit.yml/badge.svg?branch=main)
![molecule](https://github.com/chronicc/ansible-collection-bouquet/actions/workflows/molecule.yml/badge.svg?branch=main)

Setup and manage containerized applications with docker-compose.

## Requirements

The below requirements are needed on the host that executes this module.

- Docker API >= 1.25
- Docker SDK for Python >= 1.8.0
- PyYAML >= 3.11
- docker-compose >= 1.7.0, < 2.0.0

## Dependencies

- [community.docker](https://github.com/ansible-collections/community.docker)

## Roles

- [bouquet_stack](./roles/bouquet_stack/) - Setup and manage bouquet stacks.

## Development

### Changelog

The repository uses [antsibull-changelog](https://ansible.readthedocs.io/projects/antsibull-changelog/)
to create a changelog.

To update the changelog:

* Create a yaml file inside the `changelogs/fragments` directory.
* Optionally, validate your changelog fragments: `antsibull-changelog lint`.
* Generate the changelog for your release:
    `antsibull-changelog release [--version version_number]`.

## License

MIT

Author Information
------------------

- chronicc <hello@chroni.cc>
