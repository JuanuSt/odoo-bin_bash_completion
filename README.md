# odoo-bin_bash_completion
Bash completion file for command odoo-bin (odoo v10)

The command odoo-bin in Odoo has many options, but I have only created a few of them, just the ones I use most. However, it is easy to add more, so you can add your most used options.

At the start of the file, you have to set the variable db_owner, the owner of your databases. The default user is "odoo10" (this completion file is thought for a developer's machine, not for a production environment).

If you don't have the odoo-bin executable file in your $PATH, you can add an alias to your .bash_aliases file in order to use the completion file:
`
alias odoo-bin="/path/to/odoo-bin "
`
Observe the blank space at the end.

After copying the bash completion file to /etc/bash_completion.d directory and source your shell you can use TAB:
- After odoo-bin command to chose between -d or shell options.
- After **-d/shell** to chose among owner's databases.
- After **-d $database** to chose between -i (install) or -u (update) a module.
- After **-d $database -u** to chose among the modules installed in this $database.
- After **-d $database -i** to chose among the modules not installed in this $database.
- After **-d $database -i/-u $module** to complete with --stop-after-init option.
