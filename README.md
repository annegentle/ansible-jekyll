ansible-jekyll
=============

Install simple nginx instance with a Jekyll build off a bare git repo.
[Credit goes out to this awesome blog post](https://www.digitalocean.com/community/tutorials/how-to-deploy-jekyll-blogs-with-git)

#### Execute

First, copy the group_vars/jekyll.yml to a local group_vars/jekyll.yml file and customize the variables to your needs.

```bash
ansible-playbook site.yml
```

To make this work with a given OpenStack cloud, you must set the group_vars/jekyll.yml file to have the name of the remote user (cloud-user or cloud, for example) and you must have your public key loaded as a keypair to the cloud so that you can clone git repositories.

Then, to deploy a Jekyll site to your new server:

```bash
git remote add prod git@example.org:repos/example-repo.git
git push prod master
```
