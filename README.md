# Ansible role: Localization

Only tested on Archlinux.

See [archlinux locale](https://wiki.archlinux.org/title/Locale) to learn.

## Usage
Override [defaults](https://github.com/lunics/ansible_role_localization/blob/main/defaults/main.yml)
```yaml
timezone: America/New_York

locales:                  # locales generated
  - name:  en_US.UTF-8    # generate US
  - name:  cs_CZ.UTF-8    # generate Czech
    state: present
  - name:  de_CH.UTF-8    # remove Chinese
    state: absent

locales_conf:             # locales enabled
  LANG:    en_US.UTF-8    # programs in US language
  LC_TIME: cs_CZ.UTF-8    # system time in Czech format

keymap:
  KEYMAP: de-latin1       # German keyboard
  FONT:   eurlatgr        # German console
```
