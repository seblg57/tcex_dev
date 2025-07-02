# OpenSearchCheck - ThreatConnect Playbook App

## Overview

OpenSearchCheck is a custom Playbook App designed for ThreatConnect to perform comprehensive health checks and statistics collection on an OpenSearch cluster.

This app connects to your OpenSearch cluster and retrieves key information about cluster health, node status, shard distribution, and index-specific metrics.

---

## Features

- Checks cluster health status (`green`, `yellow`, `red`)
- Retrieves number of nodes in the cluster
- Reports active primary shards, active shards, unassigned shards, and percentage of active shards
- Fetches document statistics (`docs.count`, `docs.deleted`, `store.size`) for the `orgs` index
- Counts total shards across the cluster
- Supports Basic Authentication with optional username and password

---

## Inputs

| Input Name | Description                          | Required | Notes                        |
|------------|------------------------------------|----------|------------------------------|
| `os_url`   | Full OpenSearch cluster URL (e.g., `https://your-opensearch:9200`) | Yes      | Must include protocol and port |
| `os_user`  | Username for Basic Auth (optional) | No       | Required if `os_pass` provided |
| `os_pass`  | Password for Basic Auth (optional) | No       |                              |

---

## Outputs

| Output Name                  | Description                            |
|-----------------------------|------------------------------------|
| `opensearch.status`          | Cluster health status (`green`, `yellow`, `red`) |
| `opensearch.nodes`           | Number of nodes in the cluster       |
| `opensearch.active_primary_shards` | Count of active primary shards    |
| `opensearch.active_shards`   | Count of active shards                |
| `opensearch.unassigned_shards` | Count of unassigned shards          |
| `opensearch.active_shards_percent` | Percentage of active shards        |
| `opensearch.orgs_docs_count` | Document count in the `orgs` index   |
| `opensearch.orgs_docs_deleted` | Deleted documents count in `orgs`   |
| `opensearch.orgs_store_size` | Store size of the `orgs` index       |
| `opensearch.shards_count`    | Total number of shards in the cluster |

---

## Usage

1. Deploy the app to ThreatConnect.
2. Configure inputs (`os_url`, `os_user`, `os_pass` if needed) for admin user.
3. Run the playbook to retrieve real-time OpenSearch cluster status.
4. View outputs and logs for detailed cluster insights.

---

## Requirements

- ThreatConnect version 7.2.0 or higher
- Python 3.11
- TCEx SDK version 4.x

---

## Author

HexGuard Labs – Custom ThreatConnect Automation and Apps

---

Feel free to ask if you want me to tailor this README with badges, screenshots, or usage examples!
