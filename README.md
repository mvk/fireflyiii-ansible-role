# aws-ffiiiweb

Sets up firefly-iii using AWS

## Requirements

* DB details need to be known
    * DB is created using mvk.ffiii-db


## Role Variables

| Name                         | Default    | Description                         |
|:-----------------------------|:-----------|:------------------------------------|
| `mvk_fireflyiii_db_type`     | `mysql`    | supported: rds db                   |
| `mvk_fireflyiii_db_username` | `firefly`  | better replace and put into a vault |
| `mvk_fireflyiii_db_password` | `f1r3flY!` | better replace and put into a vault |
| `mvk_fireflyiii_db_schema`   | `firefly`  |                                     |
| `mvk_fireflyiii_dns_domain`  | -          | optional: if you need to upd hosts  |
| `mvk_fireflyiii_ip_address`  | -          | optional: if you need to upd hosts  |


## Dependencies

your target machine should be tagged, so that ec2.py can find it


## Example Playbook

Assuming it has a tag "Role" with value "firefly"

    - hosts: tag_Role_firefly
      roles:
      - role: mvk.aws-ffiiiweb

# License

BSD

# Author Information

Max Kovgan <max@opsguru.io>
