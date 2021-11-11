## Build's a Single VM

Modify `inventory.yaml` to suit.

Get required roles:

```bash
ansible-galaxy install -r requirements.yml --roles-path=`pwd`/roles
```

Run the `setup.yaml` playbook

```bash
ansible-playbook -i inventory.yaml setup.yaml --ask-become-pass
```

To trash the setup, use the `teardown.yaml` playbook.

```
ansible-playbook -i inventory.yaml teardown.yaml --ask-become-pass
```
