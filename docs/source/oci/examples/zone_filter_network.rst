.. _zonefilternetwork:

Zone - Filter all the zone based on a tag
=========================================

The following example policy will filter all the zones in the tenancy based on a specified tag

.. code-block:: yaml

    policies:
    - name: filter-zone
      description: |
        Filter all the zone in the tenancy based on a tag
      resource: oci.zone
      filters:
       - type: value
         key: 'freeform_tags.cloud_custodian'
         value: 'true'
         op: eq
