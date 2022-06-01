
Dump github action variables and secrets

```
- name: 'Dump Env and Secrets'
        uses: allenarceneaux/dump-vars@main
        with:
          the_secrets: ${{ toJson(secrets) }} 
```