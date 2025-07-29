📦 Splunk Query for Tracking Loading and Handling Units in DH Sort Area – Site ZLXH
This Splunk SPL query is designed to track the creation and validation of Loading Units (LU) and Handling Units (HU) at the ZLXH site within a Direct Handling (DH) sort area. It serves to correlate LU creation events (newconscreated) with subsequent validation events (validate*), enriching the data with contextual metadata such as tracking number, scan time, device ID, operator ID, and destination.

🔧 Key Features:
Multi-source correlation: Joins application logs and equipment logs to correlate LU creation with validation scans.

Dynamic JSON parsing: Extracts nested fields from message payloads using json_extract.

Sort area classification: Uses a lookup table to filter only Direct Handling areas (DH).

Field enrichment: Captures detailed info like origin, destination, scan user, scan device, scan timestamp, sort plan, and sort rules.

Data quality filtering: Excludes invalid or malformed barcodes to ensure clean analytics.

Deduplication & statistics: Ensures unique LUs are presented with latest associated data for reporting and visualization.

✅ Use Cases:
Visual dashboards for warehouse performance

Operational audit and traceability

Debugging loading unit scan issues

Ensuring completeness of parcel tracking and sorting operations
