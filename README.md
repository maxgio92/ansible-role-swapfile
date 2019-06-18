# ansible-role-swapfile

Ansible role to manage swapfile on Linux.

## Usage

```yaml
- hosts: all
  tasks:
    - include_role:
        name: swapfile
      vars:
      # ...
```
  
### Available variables

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| configure| Set to false if you want to check without configure | bool | yes | no |
| debug | Set to true to debug | bool | no | no |
| min\_disk\_free\_space | Minimum free space to left on the related device when calculating the right size of the swapfile | float | 0.25 | no |
| skip\_pre\_checks | Set to true if you don't want to check if a swap is already configured | bool | no | no |
| swap\_file\_path | The path of the swapfile | string | '/swapfile' | no |
| swap\_file\_size\_mb | The size of the swapfile in MB | int | 4096 | no |
| swappiness | The value of the swappiness to configure | int | 60 | no |
