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
# non existent path
cert_path: /tmp/certs
cert_name: ansible
# private key enabled to the repo, must be readable
# only from the owner (chmod 400)
git_key: id_rsa
git_url: github.com/myprofile/myprivaterepo
git_branch: master
```
