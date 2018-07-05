
dracclient
=================

Library for managing machines with Dell iDRAC cards.


Usage：client = client.DRACClient('1.2.3.4', 'root', 'calvin')

由于默认端口为443、默认协议为https，在未添加证书验证情况下，禁用urllib3警告的方法：
import urllib3
urllib3.disable_warnings()


Client API
  Power management
    get_power_state
    set_power_state
  Boot management
	list_boot_modes
	list_boot_devices
	change_boot_device_order
  BIOS configuration
	list_bios_settings
	set_bios_settings
	commit_pending_bios_changes
	abandon_pending_bios_changes
  RAID management
	list_raid_controllers
	list_virtual_disks
	list_physical_disks
	create_virtual_disk
	delete_virtual_disk
	commit_pending_raid_changes
	abandon_pending_raid_changes
  Inventory Management
	list_cpus
	list_memory
	list_nics
  Job management
	list_jobs
	get_job
	create_config_job
	delete_pending_config
  Lifecycle controller management
	get_lifecycle_controller_version



