# Splunk Searches
“index=* 'Failed password' | stats count by host, user, src”

## Basic SSH Failure Search
index=* "Failed password"

## Field Extraction Test
index=* "Failed password"
| stats count by host, user, src
