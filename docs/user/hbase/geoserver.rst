Using the HBase Data Store in GeoServer
=======================================

.. note::

    For general information on working with GeoMesa GeoServer plugins,
    see :doc:`/user/geoserver`.

From the main GeoServer page, create a new store by either clicking
"Add stores" in the middle of the **Welcome** page, or anywhere in the
interface by clicking "Data > Stores" in the left-hand menu and then
clicking "Add new Store".

If you have properly installed the GeoMesa HBase GeoServer plugin as described
in :ref:`install_hbase_geoserver`, "HBase (GeoMesa)" should be included in the list
under **Vector Data Sources**. If you do not see this, check that you unpacked the
plugin JARs into in the right directory and restart GeoServer.

On the "Add Store" page, select "HBase (GeoMesa)". The HBase data store takes a single parameter:

* **bigtable.table.name** - the name of the HBase table that stores feature type data

Other configuration information is taken from ``hbase-site.xml`` (see :ref:`install_hbase_geoserver`).

Click "Save", and GeoServer will search HBase for any GeoMesa-managed feature types.