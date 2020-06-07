# TUF自動化2020-01AnsibleVM

## 概要
このリポジトリは講義で作成するファイルなどをまとめたモノです。

## Week1
- 被管理ホストにファイルを転送(P.15)
```bash
ansible all -i hosts -m copy -a "src=./test.txt dest=/tmp/ansible_test"
```

- 被管理ホストのSSH鍵認証を無効化(P.24)
```bash
ansible-playbook -i hosts ./playbook/disable_ssh_pass_auth.yml 
```