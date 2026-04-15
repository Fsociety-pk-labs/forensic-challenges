# DataVault Challenge - MEDIUM

## Difficulty: MEDIUM ⭐⭐

A complex forensic investigation requiring multi-source correlation and analysis.

## Scenario

A disgruntled employee (john.admin) has stolen sensitive data from the company's database. The theft occurred across multiple systems and services. Your job is to analyze the comprehensive forensic evidence across four different log sources to piece together the attack timeline and extract the flag hidden within the evidence.

## Files Provided

- `access.log` - User access and authentication logs
- `db_audit.log` - Database activity and query audit logs
- `emails.log` - Email system logs showing data exfiltration
- `network.log` - Network traffic and connection logs

## Objective

Investigate the theft by:
1. Identifying the suspicious user and attack timeline
2. Finding the geographic anomaly indicating compromise
3. Tracing privilege escalation events
4. Locating data exfiltration evidence
5. Correlating evidence across all 4 logs
6. Extracting the hidden flag from the combined evidence

## Instructions

1. Examine all four log files systematically
2. Create a timeline of events across different log sources
3. Identify the threat actor and their actions
4. Look for flag fragments hidden throughout the logs
5. Correlate fragments using file references and metadata hashes
6. Reconstruct the complete flag

## Flag Format

`fsociety{...}`

## Hints

- The attacker is a legitimate user with unusual access patterns
- Geographic location mismatch indicates compromise
- Flag is NOT in plain text - it's fragmented across logs
- Look for:
  - Metadata fields (auth_chain, auth_token, audit_hash, session_id, final_hash, checksum)
  - File references and attachment names
  - Authentication data and transfer tokens
- Cross-reference information between all four log files
- Piece together fragments from different fields to form the complete flag

## Difficulty Breakdown

- **Analysis Complexity**: High
- **Correlation Required**: 4 files
- **Encoding Level**: Scattered fragments across metadata fields
- **Pattern Recognition**: Complex attack chain with multiple stages
- **Time Estimate**: 45-90 minutes

## Attack Chain

```
1. Legitimate login from NY (normal behavior)
2. Geographic anomaly - login from Moscow  
3. Privilege escalation to DBA role
4. Large database query and data export
5. Email-based data exfiltration
6. Malware C2 communication attempts
7. Cleanup and disconnection
```

This is an advanced challenge. Good luck, investigator!
