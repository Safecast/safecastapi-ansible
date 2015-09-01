# safecast api ansible playbooks

## Usage

Keys are encrypted using ansible-vault.

Get the latest `.vault_pass.txt` from a team member and run `chmod 600 .vault_pass.txt` to help ensure it remains a secret.

Then in your shell config add

```
export ANSIBLE_VAULT_PASSWORD_FILE=.vault_pass.txt
```

Next set up your hosts file by copying `hosts.example` to `hosts` and optionally adding your sudo password for safecast's infrastructure to the new file.

Once this is all set you should be able to run a dev deployment with:

```console
> ansible-playbook playbooks/dev.yml
```
