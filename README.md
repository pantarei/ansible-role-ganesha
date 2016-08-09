Ansible Role for NFS-Ganesha
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-nfs-ganesha.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-nfs-ganesha)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-nfs-ganesha.svg)](https://github.com/pantarei/ansible-role-nfs-ganesha)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-nfs-ganesha.svg)](https://github.com/pantarei/ansible-role-nfs-ganesha/blob/master/LICENSE)

Ansible Role for NFS-Ganesha Installation.

Requirements
------------

This role require Ansible 2.0 or higher.

This role was designed for Ubuntu Server 14.04 LTS and Ubuntu Server 16.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ganesha_idmapd_domain</td>
<td>yes</td>
<td>localdomain</td>
<td></td>
<td>The local NFS-Ganeshav4 domain name.</td>
</tr>
<tr class="even">
<td>ganesha_idmapd_nobody_group</td>
<td>yes</td>
<td>nogroup</td>
<td></td>
<td>Local group name to be used when a mapping cannot be completed.</td>
</tr>
<tr class="odd">
<td>ganesha_idmapd_nobody_user</td>
<td>yes</td>
<td>nobody</td>
<td></td>
<td>Local user name to be used when a mapping cannot be completed.</td>
</tr>
<tr class="even">
<td>ganesha_need_sggd</td>
<td>yes</td>
<td>no</td>
<td></td>
<td>Do you want to start the gssd daemon? It is required for Kerberos mounts.</td>
</tr>
<tr class="odd">
<td>ganesha_need_statd</td>
<td>yes</td>
<td>no</td>
<td></td>
<td>Do you want to start the statd daemon? It is not needed for NFS-Ganeshav4.</td>
</tr>
<tr class="even">
<td>ganesha_need_svcgssd</td>
<td>yes</td>
<td>no</td>
<td></td>
<td>Do you want to start the svcgssd daemon? It is only required for Kerberos exports.</td>
</tr>
<tr class="odd">
<td>ganesha_rpc_mountd_opts</td>
<td>yes</td>
<td>--manage-gids</td>
<td></td>
<td>Options for rpc.mountd.</td>
</tr>
<tr class="even">
<td>ganesha_rpc_ganeshad_count</td>
<td>yes</td>
<td>8</td>
<td></td>
<td>Number of servers to start up.</td>
</tr>
<tr class="odd">
<td>ganesha_rpc_ganeshad_opts</td>
<td>yes</td>
<td></td>
<td></td>
<td>Options for rpc.ganeshad.</td>
</tr>
<tr class="even">
<td>ganesha_rpc_ganeshad_priority</td>
<td>yes</td>
<td>0</td>
<td></td>
<td>Runtime priority of server.</td>
</tr>
<tr class="odd">
<td>ganesha_rpc_svcgssd_opts</td>
<td>yes</td>
<td></td>
<td></td>
<td>Options for rpc.svcgssd.</td>
</tr>
<tr class="even">
<td>ganesha_statd_opts</td>
<td>yes</td>
<td></td>
<td></td>
<td>Options for rpc.statd.</td>
</tr>
<tr class="odd">
<td>ganesha_exports</td>
<td>yes</td>
<td><a href="https://github.com/pantarei/ansible-role-ganesha/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td></td>
<td>A list of exports in &quot;folder&quot;: &quot;options&quot; style.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: hswong3i.ganesha

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-nfs-ganesha/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <a href="https://twitter.com/hswong3i" class="uri" class="uri">https://twitter.com/hswong3i</a>
    -   <a href="https://github.com/hswong3i" class="uri" class="uri">https://github.com/hswong3i</a>

