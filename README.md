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
- dnac_distribution_check_delay (default 15, delay between checks)
- dnac_batch_fail_threshold (default 2, how many unreachable devices should cause the batch to fail and execution stop)
