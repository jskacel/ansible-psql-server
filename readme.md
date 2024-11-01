## ansible-psql-server
Playbook to install PostreSQL server

## Requirements
Collections:
- ansible.posix
- community.postgresql

## Variables:
```
    psql_version: "15" # or 13
    psql_databases:
     - username: "someuser"
       password: "secretpassword"
       database: "somedatabase"
    #  - username: "anotheruser"
    #    password: "secretpassword"
    #    database: "anotherdatabase"
    psql_source_ip: "0.0.0.0/0" # this should be changed to IP or range from where you want to connect
```

## Running it
```
ansible-playbook -i inventory playbook.yml
```