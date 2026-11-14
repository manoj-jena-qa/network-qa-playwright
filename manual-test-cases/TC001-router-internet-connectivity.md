# TC001: Verify Internet Connectivity Through a Router

**Priority:** High
**Test type:** Manual functional test
**Status:** Not executed

## Objective
Verify that a computer connected to the router can access the internet.

## Preconditions
- Router is powered on.
- Router WAN port is connected to an active internet service.
- Computer is connected to a router LAN port using Ethernet.
- Computer is configured to obtain an IP address automatically.

## Test Steps and Expected Results

| Step | Action | Expected Result |
|---|---|---|
| 1 | Check the computer's Ethernet connection. | Ethernet connection is active. |
| 2 | Run `ipconfig` on Windows. | Ethernet adapter has a valid IP address, subnet mask, and default gateway for the test network. |
| 3 | Run `ping <default-gateway-IP>` using the gateway shown in step 2. | Router responds if ICMP replies are enabled. |
| 4 | Run `nslookup example.com`. | DNS lookup returns an address without a lookup error. |
| 5 | Open https://example.com in a browser. | Page loads successfully over HTTPS. |

## Actual Result
Not executed.

## Evidence
Add command outputs and screenshots after execution.
Remove public IP addresses and personal information before uploading.

## Troubleshooting Notes
- A 169.254.x.x IPv4 address can indicate failure to obtain a DHCP lease.
- If gateway ping fails, check the cable, adapter, and router settings.
- A failed ping alone does not prove connectivity is broken; ICMP may be blocked.
- If DNS lookup fails, check DNS configuration and service availability.
