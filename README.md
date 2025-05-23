# tp3-devops
## 3-2 - Playbook avec rôles

Nous avons externalisé l'installation de Docker dans un rôle Ansible (`roles/docker`), puis appelé ce rôle dans un playbook principal (`site.yml`) :

**site.yml**
```yaml
- hosts: all
  gather_facts: true
  become: true

  roles:
    - docker