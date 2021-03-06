Terraform 101
=============


Main commands:
-------------
*  init          Prepare your working directory for other commands
*  validate      Check whether the configuration is valid
*  plan          Show changes required by the current configuration
*  apply         Create or update infrastructure
*  destroy       Destroy previously-created infrastructure


All other commands:
-------------------
*  console       Try Terraform expressions at an interactive command prompt
*  fmt           Reformat your configuration in the standard style
*  force-unlock  Release a stuck lock on the current workspace
*  get           Install or upgrade remote Terraform modules
*  graph         Generate a Graphviz graph of the steps in an operation
*  import        Associate existing infrastructure with a Terraform resource
*  login         Obtain and save credentials for a remote host
*  logout        Remove locally-stored credentials for a remote host
*  output        Show output values from your root module
*  providers     Show the providers required for this configuration
*  refresh       Update the state to match remote systems
*  show          Show the current state or a saved plan
*  state         Advanced state management
*  taint         Mark a resource instance as not fully functional
*  untaint       Remove the 'tainted' state from a resource instance
*  version       Show the current Terraform version
*  workspace     Workspace management
*  reference - https://www.terraform.io/docs/cli/commands/state/show.html 

Options
--------
Global options (use these before the subcommand, if any):
  -chdir=DIR    Switch to a different working directory before executing the
                given subcommand.
  -help         Show this help output, or the help for a specified subcommand.
  -version      An alias for the "version" subcommand.


How-to:
-------
* How to pass variables example:
  - terraform plan --var-file="./sample1.tf.vars" --out myplan

* How to apply with auto-approve:
  - terraform apply --var-file="./sample1.tf.vars" -auto-approve

* How to apply a generated plan 
  - terraform apply "myplan" -auto-approve

