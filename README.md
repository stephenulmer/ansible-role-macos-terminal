# Ansible Role to Configure macOS Terminal

## Usage

Add custom Terminal.app profiles to the configuration file and/or
select the default Terminal profile.

Example playbook usage:
```
- name: Customize Terminal.app
  hosts: all
  vars:
    terminal_add_profiles:
      - "Ulmer.terminal"
    terminal_default_profile: "Ulmer"
  roles:
    - ansible-role-macos-terminal
```

## Role Configuration Variables

**terminal_add_profiles** - A list of names of profile files (exported previously or downloaded)
to install into the current user's Termninal.app preferences. The
name of the file (without the extension) is used to name the profile.

**terminal_default_profile** - The name of the profile to use automatically. It does *not* need
to be one of the ones added in **terminal_add_profiles** -- it
can be built-in, or added some other way.


## License

MIT, see LICENSE file.


## Author

Created in 2019 by Stephen Ulmer.
