# LogHunter Challenge - EASY

## Difficulty: EASY ⭐

A straightforward forensic challenge requiring log analysis and correlation.

## Scenario

A system has been compromised through brute force attack followed by privilege escalation. Your job is to analyze the logs and identify the flag hidden within the attack timeline.

## Files Provided

- `system.log` - System authentication and command execution logs
- `firewall.log` - Network connection and security events

## Objective

Analyze the logs to:
1. Identify the attack pattern (brute force → successful login → privilege escalation)
2. Locate the flag fragments hidden in the logs
3. Combine the fragments to form the complete flag

## Instructions

1. Examine both log files carefully
2. Look for suspicious patterns and timing correlations
3. Identify all flag-related fragments in the logs
4. Piece together the flag from the fragments found

## Flag Format

`fsociety{...}`

## Hints

- Pay attention to the timestamps and IP addresses
- Look for encoded or split flag components
- The flag fragments are scattered across both logs
- Correlation between system.log and firewall.log is key
- Check file read operations and command outputs for clues

## Difficulty Breakdown

- **Analysis Complexity**: Low to Medium
- **Correlation Required**: 2 files
- **Encoding Level**: Simple base64/text fragments
- **Time Estimate**: 15-30 minutes

Good luck, analyst!
