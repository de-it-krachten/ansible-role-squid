[![CI](https://github.com/de-it-krachten/ansible-role-squid/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-squid/actions?query=workflow%3ACI)


# ansible-role-squid

Installs & managed squid proxy



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- SUSE Linux Enterprise 15<sup>1</sup>
- openSUSE Leap 15
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 40
- Fedora 41

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# squid port
squid_port: 3128

# list of packages
squid_packages:
  - squid

# services
squid_services:
  - squid

# Main configuration file
squid_conf: /etc/squid/squid.conf
</pre></code>

### defaults/family-Debian.yml
<pre><code>
# UNIX group
squid_group: root
</pre></code>

### defaults/family-RedHat.yml
<pre><code>
# UNIX group
squid_group: squid
</pre></code>

### defaults/family-Suse.yml
<pre><code>
# UNIX group
squid_group: squid
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'squid'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'squid'
      ansible.builtin.include_role:
        name: squid
</pre></code>
