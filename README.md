# Docker and docker-compose

Install docker from distro repo and then installs docker-compose from pip 

## Requirements

A docker capable environment

## Role Variables

Defaults to the user connecting to target.

| var | default value | required | description |
|-----|---------------|----------|-------------|
| `DOCKER_USERS` | `["{{ansible_env.USER}}"]` | yes | List of all users that should be enable to run docker without sudo |

## Dependencies

Depends on another role called `pip`.

## Example Playbook

Example of how to use this role:

    - hosts: localhost
      roles:
         - role: mashimom.docker
           DOCKERUSERS: [kirk,picard]

## License

MIT

## Author Information

@mashimom