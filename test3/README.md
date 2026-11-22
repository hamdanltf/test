# test3

test3

## What's included

### Ansible collections

| Collection | Version | Source |
|---|---|---|
| infra.windows_ops | 2.1.0 | Private Automation Hub (validated) |



## Details

- **Tags:** `execution-environment`

- **Image registry:** `ansible-automation-platform.apps.home.hamdan.lab/podman pull ansible-automation-platform.apps.home.hamdan.lab:pah`

## Use this execution environment

If your EE uses collections from private sources (Automation Hub, private automation hub), update the token settings in `ansible.cfg` before building.


Log in to the registry and pull the image:

```bash
podman login ansible-automation-platform.apps.home.hamdan.lab
podman pull ansible-automation-platform.apps.home.hamdan.lab/podman pull ansible-automation-platform.apps.home.hamdan.lab:pah
```

If the registry uses a self-signed certificate, you may need to append `--tls-verify=false` to each `podman` command.

To use it in Ansible Automation Platform:

1. Go to **Automation Execution** > **Infrastructure** > **Execution Environments**.
2. Click **Create execution environment** and enter the image URL: `ansible-automation-platform.apps.home.hamdan.lab/podman pull ansible-automation-platform.apps.home.hamdan.lab:pah`
3. Select this execution environment in your job templates.

## Build details

- **Base image:** `registry.redhat.io/ansible-automation-platform/ee-minimal-rhel9:2.18`
- **Definition file:** `test3.yml`
- **Template file:** `test3-template.yml` - import this into Ansible automation portal to let others create EEs from the same starting point.

To make changes, use this EE's template in Ansible automation portal or rebuild manually with `ansible-builder` and the definition file.
