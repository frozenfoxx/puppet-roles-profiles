# puppet-roles-profiles
This repository is an example of how to set up a Puppet repository for the "roles and profiles" programming pattern.  The contents are:

* `dist`:  this directory contains modules designed as a part of the repo.
* `manifests`:  the master logic of the repository is called here.
 * `manifests/site.pp`:  this is the default file that defines *nodes* and assigns them each __one and only one__ *role*.
* `modules`:  this directory is automatically created if deployed with r10k.
* `site`:  within this are the roles and profiles.
 * `site/profiles/manifests`:  *profiles* that do actual units of work are kept in this directory.
 * `site/role/manifests`:  *roles* are overall classes nodes can fit into and contain multiple *profiles*.
