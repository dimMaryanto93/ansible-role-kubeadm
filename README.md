`dimmaryanto93.kubeadm`
=========

Repository ini digunakan untuk menginstall `kubeadm` untuk Linux

Support platform

- Debian
- Ubuntu
- CentOS


Ansible - User Guide
------------

Persiapan yang harus di lalukan, diantaranya

1. Create new user on your server, Recomend using **very-very Strong Password** or using password generator. 
  ```bash
  adduser <username>
  ```

2. Granted to sudoers with NOPASSWD, using `visudo`
  ```ini
  username    ALL=(ALL) NOPASSWD:ALL
  ```

3. Authenticate with private-key for login ssh, generate ssh key on your local machine then use `ssh-copy-id user@your-ip-server` to copy public key to your server.


Requirements
------------

Untuk menggunakan role ini, kita membutuhkan collection/plugins seperti berikut:

```bash
ansible-galaxy collection install community.general ansible.posix
```

Atau temen-temen bisa menggunakan `requirements.yaml` file and install menggunakan `ansible-galaxy collection install -r requirements.yaml`, dengan format seperti berikut:

```yaml
collections:
  - community.general
  - ansible.posix
```

Role Variables
--------------

None

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```ansible
- hosts: servers
  become: true
  roles:
      - { role: dimmaryanto93.kubeadm }
```

License
-------

MIT
