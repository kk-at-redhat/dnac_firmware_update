= Parameters

DNAC connection parameters. In AAP these will be a custom credential:
- dnac_host (required, without https)
- dnac_username (required)
- dnac_password (required)
- dnac_verify (optional, set false to ignore self-signed SSL certificate)

Inventories. In AAP these will be extra_vars:
- dnac_tag_to_update (string)
- dnac_hosts_to_update_url (URL with text file containing list of hosts)
- dnac_rollout_strategy (ex. {batch1_size: 2, batch2_size: 10, dynamic_batch_size: 100} - first batch will be 2 hosts, second one - 10 more hosts, the rest - 100 hosts each)

Distribution. In AAP these can be extra_vars:
- dnac_distribution_check_delay (delay between checks)
- dnac_distribution_max_time_initial (default 3300, max time in seconds to wait before moving to second batch)
- dnac_distribution_max_time_final (default 3300, max time in seconds to wait for last batch to finish)
- dnac_distribution_max_time (default 600, max time in seconds to wait between batches)
- dnac_image_overwrite (name of the image to overwrite golden image)

Activation. In AAP these can be extra_vars:
- dnac_activation_check_delay (delay between checks)
- dnac_activation_max_time_initial (default 3300, max time in seconds to wait before moving to second batch)
- dnac_activation_max_time_final (default 3300, max time in seconds to wait for last batch to finish)
- dnac_activation_max_time (default 600, max time in seconds to wait between batches)
- dnac_image_overwrite (name of the image to overwrite golden image)
- dnac_perform_activation (default false)
- odyssey_host (required, without https)
- odyssey_username (required)
- odyssey_password (required)
- odyssey_verify (optional, set false to ignore self-signed SSL certificate)
- odyssey_change_id (change ticket)
- odyssey_delay (delay in seconds between checking Odyssey for pre-activation results)
- odyssey_max_time (max total time in seconds for checking Odyssey for pre-activation results)
