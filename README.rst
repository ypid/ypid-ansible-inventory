ypid-ansible-inventory
======================

    When the default settings of DebOps_ are not paranoid enough.

This git repository tracks the public Ansible_ inventory used by ypid.
The inventory files are structured to allow interested fellows to symlink them
into their own Ansible projects.
This way, you can easily pull updates of this repository.

Note that using those settings is intended for advanced Ansible_ and DebOps_
users.

ypid-ansible-inventory is part of ypid-ansible-common_.

Disclamer
---------

About the catch line at the top of this README. ypid is a `DebOps Developer`_
and if there is anything which is considered weak or not state of the art in
DebOps_ defaults then it will be fixed in DebOps_.

File naming
-----------

All files and groups are prefixed with ``public_ypid_`` to prevent accidental
disclosure of settings that ypid would like to keep private and to introduce a
namespacing for use in Ansible host groups.

Furthermore, the following prefixes are used:

``defaults``
  Default settings of ypid.

``paranoid``
  Maximum security settings even at the risk of dropping support for not
  up-to-date software/systems and reduced convenience.
  For example Putty_ is not known to work with the paranoid ssh server
  configuration.

``qubes``
  Optimized for use together with `Qubes OS`_ VMs.

Why not make them DebOps defaults?
----------------------------------

The main reason is that the settings in this repository come at a certain cost
either in convenience and/or compatibility.
DebOps has to make a trade-off between those costs and security. There is
nothing wrong with that because the most secure system would be arguably some
mostly offline, air gapped system only running trustworthy Free Software (not
to forget handmade based on Free Hardware Designs). The generic use of such
system might be limited.  See where ypid is going with this?  DebOps defaults
are reasonable and secure defaults as far as ypid can tell.


.. _Putty: http://www.putty.org/
.. _Ansible: https://www.ansible.com/

.. Redundant definition inlined from: https://github.com/debops/docs/blob/master/docs/includes/80post.rst
.. _DebOps: https://debops.org/
.. _Qubes OS: https://www.qubes-os.org/
.. _ypid-ansible-common: https://github.com/ypid/ypid-ansible-common/
.. _DebOps Developer: https://docs.debops.org/en/latest/debops-keyring/docs/entities.html#debops-keyring-role-developers
.. ]]]
