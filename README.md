# Ansible role: Localization

Only tested on Archlinux.

See [archlinux locale](https://wiki.archlinux.org/title/Locale) to learn.

## Usage
See [defaults](https://github.com/lunics/ansible_role_localization/blob/main/defaults/main.yml)
```yaml
timezone: America/New_York

locales:  # generate US English and Czech languages and remove chinese
  - name:  en_US.UTF-8
  - name:  cs_CZ.UTF-8
    state: present
  - name:  de_CH.UTF-8
    state: absent

locales_conf:
  LANG:    en_US.UTF-8
  LC_TIME: cs_CZ.UTF-8    # time in Czech format

keymap:   # German keyboard and console
  KEYMAP: de-latin1
  FONT:   eurlatgr
```
