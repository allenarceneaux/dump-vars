
Dump github action variables and secrets

```
- name: 'Dump Env and Secrets'
        uses: allenarceneaux/dump-vars@main
        with:
          the_secrets: ${{ toJson(secrets) }} 
```

Or use standalone

```
name: Dump

on: [ push, workflow_dispatch ]

jobs:
  dump:
    runs-on: ubuntu-latest
    steps:
      - name: dump
        uses: allenarceneaux/dump-vars@main
        with:
          the_secrets: ${{ toJson(secrets) }} 
```
