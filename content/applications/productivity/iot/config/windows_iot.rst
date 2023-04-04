===============================================================
Use Windows IoT software to connect devices to an Odoo database
===============================================================

A Virtual IoT box is a computer program that needs to be downloaded and installed on a Windows
computer. This requires a Windows operating system with an Odoo 16 or later database.

The Windows Virtual :abbr:`IoT (Internet of Things)` box works the same way as a physical
:abbr:`IoT (Internet of Things)` box, with the ability to run most of the same devices. All
:abbr:`POS (Point of Sale)` devices work with it, such as a scale or printer. Payment terminals will
also work, but it should be noted that :abbr:`MRP (Material Requirement Planning)` devices are not
compatible. These include cameras or measurement tools.

Pre-requisites
==============

- Odoo 16 database
- :abbr:`IoT (Internet of Things)` compatible devices
- Device drivers for Windows.
- Windows computer (laptop, desktop, server)

Connect the Windows virtual Iot box to an Odoo database
=======================================================

#. Navigate to the Odoo 16 or higher installation package for Enterprise/Community Windows at
   `Odoo's Download Page <https://odoo.com/download>`_.

#. Install and setup the Odoo .exe file.

   After the instructions screen click :guilabel:`Next` to start the installation. Agree to the
   :abbr:`TOS (Terms of Service)`.

#. During the next step of the installation, select :guilabel:`Odoo IoT` from the :guilabel:`Select
   the type of install` dropdown.

   For reference, the following should be installed:

   - **Odoo server**
   - **Odoo IoT**
   - **Nginx WebServer**
   - **Ghostscript interpreter**


   Ensure there is enough space on the computer for the installation and click :guilabel:`Next`.

#. Select the :guilabel:`Destination Folder`.

   .. warning::
      Odoo's Windows virtual IoT software shouldn't be installed inside any of the Window's User's
      directories. Doing so won't allow for Nginx to initialize.

   Choosing ``C:\odoo`` as the install location will allow for the Nginx server to start. Click
   :guilabel:`Install`.

#. Allow the installation to occur. This may take a few minutes. Click :guilabel:`Next` to continue.

#. Ensure that the :guilabel:`Start Odoo` box is checked and click :guilabel:`Finish`.

#. After installation, the Odoo server will run and automatically open ``localhost:8069`` on your
   web browser. The webpage should display the :abbr:`IoT (Internet of Things)` Box configuration
   page.

#. Connect devices to Windows computer.

#. Windows should automatically detect the device because the driver is pre-installed on
   the computer. If not, search for and install the Windows driver for the device.

#. Refresh the :abbr:`IoT (Internet of Things)`  Box Configuration Page and verify the device is
   seen on the configuration page. If not, reload the handlers through the configuration page.

#. Connect Windows IoT to a database using existing instructions (manually using the Token).

   .. seealso::
      :doc:`connect`

#. Use the devices connected to :abbr:`IoT (Internet of Things)` as you normally would.


Troubleshooting
===============

Virtual Windows IoT box not showing on the database
---------------------------------------------------

In some instances a manual restart of the physical :abbr:`IoT (Internet of Things)` box can resolve
the issue. For the Windows virtual :abbr:`IoT (Internet of Things)` box a manual restart of the Odoo
server can resolve database connection issues.

To restart the virtual Windows IoT server:

#. Type "Services" into the :guilabel:`Search Bar`
#. Select the :menuselection:`Services` App and scroll down to the :guilabel:`Odoo` Service.
#. Right click on :guilabel:`Odoo` and select :guilabel:`Start` or :guilabel:`Restart`. This action
   will manually restart the Odoo IoT server.

Windows Firewall
----------------

The Windows virtual :abbr:`IoT (Internet of Things)` box software may not connect to the :abbr:`LAN
(Local Area Network)` due to the Windows Firewall preventing the connection. Consult your local IT
support to make exceptions in the :abbr:`OS (Operating System)`.


Uninstalling Windows IoT
------------------------

Uninstalling the Windows virtual :abbr:`IoT (Internet of Things)` box is done through the Windows
program manager. Search in any Windows version for ''program''. Select :guilabel:`Add or Remove
Programs` located in the control panel. Search for ``Odoo`` and click the :guilabel:`three dot menu`
to uninstall.

Confirm the uninstallation and follow the steps to uninstall through the Odoo 16.0 uninstall guide.
