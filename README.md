# PharmaNova Network Infrastructure

## Project Overview
This project contains the complete network infrastructure configuration for PharmaNova, a pharmaceutical company. The infrastructure includes DNS servers, mail servers, routers, and firewall configurations that enable secure communication between different network segments.

## Network Architecture
The network is divided into multiple segments (subnets):
- DMZ zone (192.168.5.0/24) - Contains public-facing services
- Internal networks (192.168.1.0/24 through 192.168.4.0/24, 192.168.6.0/24 through 192.168.12.0/24)
- ReteB network (192.168.2.0/24) - Contains internal DNS server

## Components

### DNS Infrastructure
- External DNS server (dns.pharmanova.it - 192.168.5.10)
- Internal DNS server (dns.reteb.pharmanova.it - 192.168.2.10)
- Forward and reverse zone configurations
- Domain resolution for pharmanova.it and dmz.pharmanova.it

### Mail Server
- Configured with Sendmail (mail.pharmanova.it - 192.168.5.4)
- SMTP, POP3, and IMAP services
- Email aliases and virtual users
- Anti-spam configurations

### Network Routing
- RouterA through RouterD for internal network routing
- RouterF for DMZ routing and NAT services
- Firewall for securing external access

### Security Features
- Access Control Lists (ACLs) on routers and firewall
- Network Address Translation (NAT) for internal hosts
- Controlled access to services through specific ports
- Spam filtering for email

## Directory Structure
- DnsEXT/ - External DNS server configurations
- DnsINT/ - Internal DNS server configurations
- Mail Server/ - Mail server configurations
- Router/ - Router and firewall configurations

## Installation & Configuration
The configuration files are organized by service and ready to be deployed on respective servers. Each configuration file includes detailed comments explaining its purpose and settings.

## Services Exposed
- DNS (port 53)
- Web (HTTP/HTTPS - ports 80/443)
- Mail (SMTP, POP3, IMAP - ports 25, 110, 143)
- Proxy (port 80)

## Networking Details
- RIP routing protocol for internal networks
- DHCP services for client networks
- DNS forwarding to Cloudflare's DNS (1.1.1.1)

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Author
Copyright (c) 2025 Danilo Palladino
