# TUF自動化2020-01AnsibleVM

## 概要
このリポジトリは講義で作成するファイルなどをまとめたモノです。

## Week2
- 初めてのRole実行(P.9)
```bash
ansible-playbook -i hosts playbook/apache.yml
```

- --start-atオプションによるplaybook開始位置制御(P.22)
```bash
ansible-playbook -i hosts playbook/apache.yml --start-at="start httpd"
```

- 値による真偽値の確認(P.35)
```bash
ansible-playbook -i hosts playbook/boolean_test.yml
```

## Week1
- 被管理ホストにファイルを転送(P.15)
```bash
ansible all -i hosts -m copy -a "src=./test.txt dest=/tmp/ansible_test"
```

- 被管理ホストのSSH鍵認証を無効化(P.24)
```bash
ansible-playbook -i hosts ./playbook/disable_ssh_pass_auth.yml 
```