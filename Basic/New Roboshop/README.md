# RoboShop Ansible - Learning Starter

A hands-on scaffold of CUSTOM ROLES you can read, run, and extend.

## What's here
- ansible.cfg          finds the inventory and roles/ folder automatically
- inventory.ini        one group per component (rename hosts to your servers)
- group_vars/all.yaml  variables shared by everything
- roboshop.yaml        the one tiny playbook: pass -e "component=NAME"
- roles/
  - demo/       smallest role (one task) - start here
  - common/     shared steps reused by app components
  - mongodb/    cleanest full example (copy + install + service + handler)
  - redis/      install + edit config + handler
  - mysql/      install + set root password (defaults variable)
  - rabbitmq/   install + create user (pattern; verify repo for your version)
  - catalogue/  example Node.js app (reuses common, template, systemd)

## Run it
    ansible-playbook roboshop.yaml -e "component=mongodb"

## Suggested reading order while learning
1. roles/demo/tasks/main.yaml       (1 task)
2. roles/mongodb/                    (the full pattern, done simply)
3. roles/redis/, roles/mysql/        (variations)
4. roles/common/ + roles/catalogue/  (reuse + app pattern)

## IMPORTANT - learning scaffold, not guaranteed production code
Some specifics change over time and per OS. Verify before trusting a run:
- Module stream names (nodejs:20, redis:7)
- Config file paths (e.g. /etc/redis/redis.conf vs /etc/redis.conf)
- RabbitMQ + Erlang repo setup
- The catalogue download URL (roles/catalogue/defaults/main.yaml)

The PATTERNS (folder layout, name-matching, handlers, become, idempotency)
are correct - that is what you are here to learn.
