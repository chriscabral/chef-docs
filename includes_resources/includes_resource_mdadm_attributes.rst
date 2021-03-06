.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.

This resource has the following attributes:

.. list-table::
   :widths: 150 450
   :header-rows: 1

   * - Attribute
     - Description
   * - ``bitmap``
     - The path to a file in which a write-intent bitmap is stored. Default value: ``nil``.
   * - ``chunk``
     - |chunk_size| This attribute should not be used for a RAID 1 mirrored pair (i.e. when the ``level`` attribute is set to ``1``). Default value: ``16``.
   * - ``devices``
     - |device mdadm| Default value: ``[]``.
   * - ``exists``
     - Indicates whether the RAID array exists. Default value: ``false``.
   * - ``level``
     - |level resource mdadm|
   * - ``metadata``
     - The superblock type for RAID metadata. Default value: ``0.90``.
   * - ``provider``
     - Optional. |provider resource_attribute|
   * - ``raid_device``
     - |raid_device mdadm| Default value: ``name``.





