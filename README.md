# selfsignedcert

The main goal is to create, update and sync your selfsigned cert with a git repository.
A private repository is needed because this include private keys. 

## Role Install
```
ansible-galaxy install --roles-path ./roles jsecchiero.selfsignedcert
```

## Example

This example generate `ansible.pem`, `ansible-key.pem`, `ansible.csr` and `ansible-bundle.pem` and put your certificate in `myprivaterepo` repository.

```
cert_path: /tmp
cert_name: ansible
git_key: id_rsa
git_url: github.com/myprofile/myprivaterepo
git_branch: master
```
