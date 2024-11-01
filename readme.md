## ansible-psql-server
Playbook to install PostreSQL server

## Requirements
Collections:
- ansible.posix
- community.postgresql

```
ansible-galaxy collection install -r requirements.yml
```
## Variables:
```
    psql_version: "15" # or 13
    psql_databases:
     - username: "someuser"
       password: "secretpassword"
       database: "somedatabase"
       sourceip: "0.0.0.0/0" # this should be changed to IP or range from where you want to connect
       extension: "" # in case of Hub, you need to add hstore
    #  - username: "anotheruser"
    #    password: "secretpassword"
    #    database: "anotherdatabase"
    #    sourceip: "0.0.0.0/0" # this should be changed to IP or range from where you want to connect
    #    extension: "" # in case of Hub, you need to add hstore
```

## Running it
```
ansible-playbook -i inventory playbook.yml
```
