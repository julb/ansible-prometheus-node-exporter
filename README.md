# prometheus-node-exporter

This role enables to install [prometheus-node-exporter](https://github.com/prometheus/node_exporter/) as a systemd service.

## Requirements

No requirements.

## Role Variables

| Name                       | Type   | Location            | Description                                                                                                  |
| -------------------------- | ------ | ------------------- | ------------------------------------------------------------------------------------------------------------ |
| node_exporter_user         | string | `defaults/main.yml` | Unix user which is created to run the node-exporter service. Defaults to `node-exporter`.                    |
| node_exporter_group        | string | `defaults/main.yml` | Unix group which is created to run the node-exporter service. Defaults to `node-exporter`.                   |
| node_exporter_listen_port  | number | `defaults/main.yml` | The port on which the node-exporter service is listening. Defaults to `9100`.                                |
| node_exporter_releases_url | string | `defaults/main.yml` | The base URL from which to download the binaries. Defaults to `https://github.com/prometheus/node_exporter`. |
| node_exporter_version      | string | `defaults/main.yml` | The version to install. Defaults to `1.1.2`.                                                                 |
| node_exporter_arch         | string | `defaults/main.yml` | The architecture of the binary to install. Defaults to `linux-amd64`.                                        |
| node_exporter_executable   | string | `vars/main.yml`     | The location at which to install the binary package. Defaults to `/usr/local/sbin/node_exporter`.            |

## Dependencies

No dependencies.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
    - { role: julb.prometheus-node-exporter }
```

## License

MIT

## Author Information

More to find on my [Github](https://github.com/julb).

## Contributing

This project is totally open source and contributors are welcome.

When you submit a PR, please ensure that the syntax has been checked.
