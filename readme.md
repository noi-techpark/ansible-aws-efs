Ansible AWS EFS
===============

Mounting AWS EFS.

## Role Variables

- `aws_efs_path`: The path where the EFS filesystem should be mounted
- `aws_efs_filesystem_id`: The filesystem id
- `aws_efs_access_point_id`: The access point id
- `aws_efs_user`: The user used for file permissions
- `aws_efs_group`: The group used for file permissions
- `aws_efs_mode`: The mode used for file permissions

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: ansible-aws-efs
      vars:
        aws_efs_path: /opt/efs
        aws_efs_filesystem_id: fs-9a7da250
        aws_efs_access_point_id: fsap-0974963b0bab587c3
```

## Versioning

In order to have a verioning in place and working, create leightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag 1.0
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d 1.0
git push origin :refs/tags/1.0
git tag 1.0
git push --tags
```
