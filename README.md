# ansible-mysql-dump

## Description

Ansible playbook to dump mysql databases in one place.

## What it do?

You define the "backup/dump" server host and directory via variable file, and the playbook would dump all the databases you define in `hosts.yaml` to that server and directory.

## File Tree

```
├── hosts.yaml
├── playbook.yaml
├── README.md
└── roles
    └── dump-mysql
        ├── tasks
        │   └── main.yaml
        └── vars
            └── main.yaml
```

## How to Use

1. Install Ansible;
2. Clone this project;
3. Move inside the project directory;
4. Edit `hosts.yaml` file and `roles/<role-name>/vars/main.yaml` according to your need;
5. Run the playbook:
```
ansible-playbook -i hosts.yaml playbook.yaml
```

## Conclusion

Your db dump should be saved in the directory you define in the variable file.
