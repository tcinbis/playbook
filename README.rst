Playbook
=========

Generic playbook for the ANTS framework. Roles can be installed
from `ansible galaxy <https://galaxy.ansible.com/ANTS-Framework/>`__

Great, what do I do with this?
--------------------------------
`Install ANTS <https://github.com/ANTS-Framework/ants>`__ if you haven't already and go through the first steps.

Once you're done, `duplicate the repository <https://help.github.com/articles/duplicating-a-repository/>`__
(you might want to make it private later on) and update your client configuration to point to it.

Edit main.yml.

Have fun.

How do I make my own playbook?
--------------------------------
The ANTS playbook is a git repository structured according to the
`ansible playbook best practices <http://docs.ansible.com/ansible/latest/playbooks_best_practices.html#directory-layout>`__.
You can duplicate it or you can create your own git repo.

Installing roles
----------------
You can add roles using `ansible-galaxy <http://docs.ansible.com/ansible/latest/galaxy.html>`__ or write your own.
We included a roles.yml in your playbook so you can add roles besides the generic\_motd already present.

.. code-block::

    ansible-galaxy install -r roles.yml --roles-path /path/to/your/roles/dir

Update Roles
------------
When roles get updated in ansible galaxy, you might want to update them
in your playbook as well. We recommend adding all your roles to
roles.yml.

By adding roles to your ansible\_roles.yml file, you can pull
the latest version of any role using the following command:

.. code-block::

    # Notice the -f flag
    ansible-galaxy install -r roles.yml -f --roles-path /path/to/your/roles/dir

This will pull the latest version of all roles, that are listed in this file.
All our roles in the master branch are stable, but you might want to 
do this in a testing branch to see how the changes behave in your environment.

You also might want to check out individual roles by tags or branches or to write your own roles.yml file.  
For more information on the file syntax, have a look at the
`official docs by ansible <http://docs.ansible.com/ansible/latest/galaxy.html#installing-multiple-roles-from-a-file>`__.
