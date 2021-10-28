scollector
=========

This roles installs and configures scollector, the telemetry collector for Bosun. It also adds the bosun-emitter helper tool, as well as jq.

[![Build Status](https://github.com/Rheinwerk/ansible-role-scollector/actions/workflows/ci.yml/badge.svg)](https://github.com/Rheinwerk/ansible-role-scollector/actions/workflows/ci.yml)

The general contract of this role is to take the variables map `_scollector` from `defaults/main.yml` as a template for your configuration and pass that configuration as a parameter to this role.


Requirements
------------

Bosun does not provide a Debian/Ubuntu repository. To use this role, you currently need to first make sure you have the bosun-scollector package available in a repository, configured in your APT sources. The same goes for the bosun-emitter. It can be found at https://packagecloud.io/lukaspustina/opensource. The `_scollector` variable (see below) offers a convenience feature to add this repo. In a future version, it might become split out into a separate role.

Role Variables
--------------

`_scollector` is a map that contains all configuration and settings for this role. `RW_APT_CACHE_UPDATE` and `RW_ENABLE_DOWNLOADS` may be specified as _extra variables_ on invocation of Ansible in order to force `apt-get update` or install the latest version of scollector, respectively. Please see `defaults/main.yml` for details.

Dependencies
------------

None.


License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Lukas Pustina](https://github.com/lukaspustina) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.
