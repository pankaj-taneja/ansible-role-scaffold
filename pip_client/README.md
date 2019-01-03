Role Name
=========

This role is used for setting up pip client pip.conf


Role Variables
--------------

```python
pip_client_host: 'pypi.python.org'
pip_client_index: "http://{{ pip_client_host }}/simple"
```

Example Playbook
----------------

Example passing variable pip_client_host and pip_client_index
```python
- name: Retrieve facts all  host
  hosts:
    - all
  gather_facts: true
  any_errors_fatal: True
  tasks: []

- name: Deploy Pip client configuration
  hosts:
    - management-nodes
  vars:
    - pip_client_host: 'pypi.python.org'
    - pip_client_index: "http://{{ pip_client_host }}/simple"
  roles:
    - pip_client
```

Below example will use default variable
```python
- name: Retrieve facts all  host
  hosts:
    - all
  gather_facts: true
  any_errors_fatal: True
  tasks: []

- name: Deploy Pip client configuration
  hosts:
    - all
  roles:
    - pip-client
```


License
-------

Guavus Inc

