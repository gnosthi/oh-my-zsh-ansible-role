Role Name
=========

Ansible Role to install and configure Oh-my-zsh.

Requirements
------------

Edit vars/main.yml and ensure that the proper user is defined.

Role Variables
--------------


* omzsh_debug - boolean : Enable role debugging
* omzsh_zsh_path - string : path of the zsh binary

The following are config related variables.
* omzsh_theme - string : oh-my-zsh theme to enable in the .zshrc config
* omzsh_state: - string : (not implemented yet) define oh-my-zsh version to use; can be 'latest' or a version number.
* omzsh_repo: - string : installer url.
* omzsh_dest: - string : path to oh-my-zsh installation directory used for $ZSH env variable in config.
* omzsh_rc_path - string : path to the users zshrc file
* omzsh_export_paths - list : list of $PATH paths to be exported in the .zshrc file
* omzsh_do_random_theme - string : 'yes'/'no' enable random theme within zshrc file
* omzsh_do_case_sensitive - string : 'yes'/'no' enable case sensitive searching in zshrc file
* omzsh_do_hyphen_insensitive - string : 'yes'/'no' disable hyphen sensitivity
* omzsh_do_disable_auto_update - string : 'yes'/'no' disable oh-my-zsh auto-update
* omzsh_do_disable_ls_colors - string : 'yes'/'no' disable ls colors in .zshrc file
* omzsh_do_disable_auto_title - string : 'yes'/'no' disable auto titleing for terminal winodws
* omzsh_do_enable_correction - string : 'yes'/'no' enable command auto-correction in .zshrc file
* omzsh_do_completion_waiting_dots - string : 'yes'/'no' enable waiting dots for command completion searching
* omzsh_do_disable_untracked_files_dirty - string : 'yes'/'no' disable completion for untracked files
* omzsh_hist_stamps - string : date and time format for history timestamps (defaults to mm/dd/yy)
* omzsh_do_zsh_customer - string : 'yes'/'no' use a customer 'custom' path other than the default path
* omzsh_custom_path - string : path to custom 'custom' path. (Ignored if omzsh_do_zsh_custom is set to no)
* omzsh_plugins_enabled - list : a list of zsh plugins to enable in the .zshrc config file.
* omzsh_source_custom_theme -  boolean : (not implemented yet) controls the running of the installation of a custom oh-my-zsh theme.
* omzsh_install_powerline_fonts - boolean : (not implemented yet) install powerline fonts for use with certain themes.
* omzsh_custom_theme - boolen : (not implemented yet) use a custom sourced theme
* omzsh_custom_theme_url - string : (not implemented yet) url to custom theme installer.
* omzsh_users - list : (not implemented yet sort of) define a list of users to install oh-my-zsh for.
* omzsh_zshrc_appends - multi-line string : any script you want appended to the zshrc file.


Dependencies
------------

The Oh-my-zsh role depends on git and zsh being installed. However these dependencies are resolved by the role itself.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - role: oh-my-zsh

License
-------

BSD
