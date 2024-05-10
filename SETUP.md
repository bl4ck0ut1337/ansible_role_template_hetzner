# SETUP
## Hetzner
### SSH Key
Add an SSH key to your Hetzner Cloud project and name it `molecule` and
Place the private key in `~/.ssh/molecule`.

### API Token
Create an API token in your Hetzner Cloud project and add it to `molecule/default/vault.yml`.

## Vault
### Vault Password File
Add a `.vaultpass` file in `molecule/default/` and insert your Ansible Vault password.

### Encrypt sensitive data
```bash
ansible-vault encrypt molecule/default/vault.yml --vault-pass-file=molecule/default/.vaultpass
```
