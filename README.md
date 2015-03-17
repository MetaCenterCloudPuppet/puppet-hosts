
#### Table of Contents

1. [Module Description](#module-description)
2. [Usage (Examples)](#usage-examples)
3. [Requirements](#requirements)

<a name="module-description"></a>
## Module Description

This module only adds entries to /etc/hosts.

<a name="usage-examples"></a>
## Usage (Examples)

**Hiera file:**
~~~
---
hosts::hosts:
  '10.168.3.0':
    fqdn: 'example1'
  '10.168.3.1':
    fqdn: 'example2'
  '10.168.3.2':
    fqdn: 'example3'
~~~

**Puppet file:**
~~~
include hosts
create_resources('hosts::add', hiera('hosts::hosts'))
~~~

<a name="requirements"></a>
## Requirements

Supported OS:

* Debian
* Ret Hat

Tested OS:

* Debian 7.3 (Wheezy)
