Ansible Role: scotch
=====================

[//]: <> (Comment)
[//]: <> (A brief description of the role goes here.)

Install [scotch](https://gitlab.inria.fr/scotch/scotch) on Centos 7 from sources.

_Work in progress_

***

Requirements
------------

[//]: <> (Any pre-requisites that may not be covered by Ansible itself 
or the role should be mentioned here. For instance, if the role uses the EC2 module, 
it may be a good idea to mention in this section that the boto package is required.
)

None

Role Variables
--------------

[//]: <> (A description of the settable variables for this role should go here,
including any variables that are in defaults/main.yml, vars/main.yml, 
and any variables that can/should be set via parameters to the role. 
Any variables that are read from other roles and/or the global scope 
\(ie. hostvars, group vars, etc.\) should be mentioned here as well.
)

Available variables are listed below, along with default values (see [`defaults/main.yml`](defaults/main.yml)):

| Variable  |  	Default  | Comments  |
|---|---|---|
| `scotch_version`   | [6.1.0](https://gitlab.inria.fr/scotch/scotch) | Choose scotch version to install  |
| `scotch_install_dir`  | /opt/scotch/  | Directory where to install scotch   |
| `scotch_module`  | false  | Create environment module  |
| `scotch_verbose`  | false  | Add some outputs in stdout |
| `scotch_make_jobs`  | 4  | Number of jobs for the build process  |
                         
Dependencies             
------------       
      
[//]: <> (A list of other roles hosted on Galaxy should go here, 
plus any details in regards to parameters that may need to be set for other roles, 
or variables that are used from other roles.
)

-- This role cannot be played independently (yet) --

*Required roles:*

- role: `korzeczl/gcc`
- role: `korzeczl/openmpi`

Example Playbook
----------------

[//]: <> (Including an example of how to use your role \(for instance, with variables passed in as parameters\) is always nice for users too:)

    - hosts: my_server
      roles:
        - role: korzeczl.gcc
        - role: korzeczl.openmpi
        - role: korzeczl.scotch 

License
-------

[//]: <> (Comment)

[MIT][link-license]

Author Information
------------------

[//]: <> (An optional section for the role authors to include contact information, 
or a website \(HTML is not allowed\).)

This role was created in 2020 by Laurent Korzeczek.

[link-license]: https://gitlab.com/ansible-roles-korzeczl/scotch/-/blob/master/LICENSE
[link-galaxy]: https://galaxy.ansible.com/korzeczl/scotch