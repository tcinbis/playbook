# Playbook
------------

*Generic playbook for the ANTS framework. All roles are included as
[git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).*


## Great, what do I do with this?
Install ants if you haven't already and go through the first steps.

Once you're done, [dublicate the repository](https://help.github.com/articles/duplicating-a-repository/)
(you might want to make it private later on) and update your client to point to it. Edit local.yml. Have fun.


## How do I make my own playbook?
The ants playbook is a git repository structured accoring to the
[ansible playbook best practices](http://docs.ansible.com/ansible/latest/playbooks_best_practices.html#directory-layout)
You can dublicate it or you can create your own git repo. We recommend adding roles as
git submodules. You'll thank us later.


## Write your own roles
### Role Best Practices
Very role should contain a README with the following sections
* Title
* Description
* Usage

You should also take care that your master branch is always stabile.
Develop in a dedicated development or feature branch.

You can also use tags and include a CHANGELOG.md in your role.


## Update Roles
When roles get updated in our ants playbook, you might want to update them
in your playbook as well. Run the following command to update all your
submodules: `git submodule update --recursive --remote`

This will pull the latest version of all roles, that are included as submodules.
All our roles in the master branch are stabile, but you might want to 
do this in a testing branch to see how the changes behave in your environment.

You also might want to check out individual submodules by tag.

