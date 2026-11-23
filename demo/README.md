# demo

demo

## What's included

### Ansible collections

No additional collections. This EE uses only what the base image provides.



## Details

- **Tags:** `execution-environment`

- **Image registry:** `docker.io/ee-builds:latest`

## Use this execution environment

If your EE uses collections from private sources (Automation Hub, private automation hub), update the token settings in `ansible.cfg` before building.


Log in to the registry and pull the image:

```bash
podman login docker.io
podman pull docker.io/ee-builds:latest
```

If the registry uses a self-signed certificate, you may need to append `--tls-verify=false` to each `podman` command.

To use it in Ansible Automation Platform:

1. Go to **Automation Execution** > **Infrastructure** > **Execution Environments**.
2. Click **Create execution environment** and enter the image URL: `docker.io/ee-builds:latest`
3. Select this execution environment in your job templates.

## Build details

- **Base image:** `registry.redhat.io/ansible-automation-platform/ee-minimal-rhel8:2.18`
- **Definition file:** `demo.yml`
- **Template file:** `demo-template.yml` - import this into Ansible automation portal to let others create EEs from the same starting point.

To make changes, use this EE's template in Ansible automation portal or rebuild manually with `ansible-builder` and the definition file.
