> 🚧 **DRAFT README** 🚧  
> This README is a work in progress and subject to change. Some information may be incomplete or inaccurate.
![Status](https://img.shields.io/badge/status-draft-yellow)


# DNS Allowlists - Essential Functionality Restoration

[![GitHub stars](https://img.shields.io/github/stars/network-security-toolkit/dns-allowlists?style=flat-square)](https://github.com/network-security-toolkit/dns-allowlists/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/network-security-toolkit/dns-allowlists?style=flat-square)](https://github.com/network-security-toolkit/dns-allowlists/network)
[![GitHub issues](https://img.shields.io/github/issues/network-security-toolkit/dns-allowlists?style=flat-square)](https://github.com/network-security-toolkit/dns-allowlists/issues)
[![License](https://img.shields.io/github/license/network-security-toolkit/dns-allowlists?style=flat-square)](LICENSE)

> **The perfect balance**: Maintain aggressive DNS blocking for maximum protection while preserving essential website functionality through a carefully curated allowlist.

## 🎯 Core Philosophy

**Block Everything, Allow Only What's Essential**

This project enables you to use the most aggressive DNS blocklists available without breaking legitimate website functionality. Instead of weakening your protection by using less comprehensive blocklists, you can deploy maximum blocking power and then surgically restore only the essential domains needed for proper operation.

### Why This Approach Works Better

- ✅ **Maximum Protection**: Use the most comprehensive blocklists without compromise
- ✅ **Precision Restoration**: Restore only verified essential functionality  
- ✅ **Zero Compromise**: No reduction in security for convenience
- ✅ **Community Verified**: Every domain validated by real-world testing

## 🚀 Quick Start

### The Two-Layer Strategy

1. **Deploy Aggressive Blocking**: Install comprehensive DNS blocklists (Energized Ultimate, Hagezi Ultimate, 1Hosts Xtra)
2. **Restore Essential Functions**: Apply this allowlist to unbreak legitimate functionality

### What Gets Restored?

Only domains that are:
- **Functionally Essential**: Required for core website operations
- **Legitimately Needed**: Not advertising, tracking, or telemetry
- **Community Verified**: Tested and validated by multiple users
- **Security Reviewed**: Manually vetted for potential risks

## 🛡️ Target Blocklist Configuration

This allowlist is specifically designed and tested to work with this exact combination of blocklists:

### Primary Blocklist Stack
- **Energized Ultimate** - Maximum protection with comprehensive blocking
- **NextDNS Ads & Trackers Blocklist** - Advanced tracking and advertising protection
- **AdGuard DNS Filter** - Comprehensive ad and tracker blocking
- **OISD** - Comprehensive malware and ad blocking
- **1Hosts (Xtra)** - Extended protection with additional coverage
- **hBlock** - Minimalist yet effective blocking solution
- **HaGeZi - Multi ULTIMATE** - Ultimate protection with multi-layered blocking
- **Steven Black** - Unified hosts file with consolidated blocking

*This specific combination provides maximum security coverage while this allowlist ensures functionality remains intact.*

## 📋 Installation Guide

### Pi-hole Implementation
```bash
# 1. Install the complete blocklist stack
pihole -b https://energized.pro/ultimate/formats/hosts.txt
pihole -b https://raw.githubusercontent.com/AdguardTeam/AdguardFilters/master/DNSFilter/sections/adservers.txt
pihole -b https://small.oisd.nl/
pihole -b https://raw.githubusercontent.com/badmojr/1Hosts/master/Xtra/hosts.txt
pihole -b https://hblock.molinero.dev/hosts
pihole -b https://raw.githubusercontent.com/hagezi/dns-blocklists/main/hosts/ultimate.txt
pihole -b https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts

# 2. Apply functionality restoration allowlist
pihole -w -l https://raw.githubusercontent.com/network-security-toolkit/dns-allowlists/main/hosts/multi.txt
```

### AdGuard Home Setup
```bash
# 1. Add all blocklists in DNS blocklists section:
# - Energized Ultimate: https://energized.pro/ultimate/formats/adguard.txt
# - NextDNS integration or manual AdGuard filter
# - AdGuard DNS Filter: Built-in or manual addition
# - OISD: https://small.oisd.nl/
# - 1Hosts Xtra: https://raw.githubusercontent.com/badmojr/1Hosts/master/Xtra/adguard.txt  
# - hBlock: https://hblock.molinero.dev/hosts
# - HaGeZi Ultimate: https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adguard/ultimate.txt
# - Steven Black: https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts

# 2. Import functionality allowlist as custom filtering rules
# URL: https://raw.githubusercontent.com/network-security-toolkit/dns-allowlists/main/hosts/multi.txt
```

### pfSense/OPNsense Configuration
```bash
# 1. Configure the complete blocklist stack in pfBlockerNG DNSBL Feeds:
# - Energized Ultimate
# - NextDNS Ads & Trackers (if supported)
# - AdGuard DNS Filter  
# - OISD
# - 1Hosts Xtra
# - hBlock
# - HaGeZi Multi ULTIMATE
# - Steven Black

# 2. Add functionality allowlist in pfBlockerNG whitelist
# URL: https://raw.githubusercontent.com/network-security-toolkit/dns-allowlists/main/hosts/multi.txt
```

## 🔧 Available Formats

| Format | File | Use Case |
|--------|------|----------|
| Universal Hosts | `hosts/multi.txt` | Compatible with Pi-hole, AdGuard Home, pfSense, OPNsense, and all major DNS filtering platforms |

*Single universal format works across all platforms - no need for separate formats!*

## 📊 Restored Functionality Categories

### 🛒 E-commerce Essentials
Critical for online shopping and transactions:
- Payment gateways (PayPal, Stripe, Square processing)
- Shopping cart and checkout functionality
- Price comparison and product reviews
- Legitimate recommendation engines

### 🔐 Authentication & Security  
Essential for secure access:
- OAuth providers (Google, Microsoft, GitHub SSO)
- Two-factor authentication services
- Secure login mechanisms
- Certificate validation services

### 💼 Business Operations
Required for legitimate business functions:
- Analytics (only essential tracking, not invasive)
- Email delivery services (transactional emails)
- Customer support systems
- Essential CRM integrations

### 🎮 Gaming & Entertainment
Core functionality for digital entertainment:
- Game launcher authentication
- Streaming service APIs (Netflix, Spotify essentials)
- Gaming platform integrations
- Content delivery for legitimate media

### 📱 Communication & Social
Essential communication features:
- Comment systems and forums
- Live chat widgets (customer support)
- Social sharing (functionality only, not tracking)
- Communication platform integrations

### 🏦 Financial Services
Critical financial platform functions:
- Banking authentication systems
- Investment platform core services
- Cryptocurrency exchange essentials
- Financial data providers (non-tracking)

## 🧪 Rigorous Vetting Process

Every domain undergoes strict evaluation:

### ✅ Inclusion Criteria
- **Functionality First**: Breaks legitimate website features when blocked
- **Security Cleared**: No malware, phishing, or suspicious activity
- **Privacy Respectful**: Not primarily for tracking or data collection
- **Thoroughly Tested**: Verified across multiple platforms and use cases
- **Documented Need**: Clear evidence of functional necessity

### ❌ Exclusion Criteria  
- Advertising networks (blocked by design)
- Tracking and analytics (unless absolutely essential)
- Telemetry and data collection services
- Social media widgets (unless core functionality)
- Any suspicious or questionable domains

## 🤝 Contributing to Maximum Security

### 🐛 Report Broken Functionality

When aggressive blocking breaks something essential:

1. **Verify It's Essential**: Confirm the domain is needed for core functionality
2. **Document the Break**: Screenshot the broken feature  
3. **Identify the Blocker**: Which aggressive list is blocking it
4. **Test Across Platforms**: Verify the issue occurs on different DNS filtering solutions
5. **Create Detailed Issue**: Include all evidence and reproduction steps

### ✨ Propose Essential Domains

Before submitting domains for allowlisting:

1. **Test Without It**: Confirm functionality actually breaks
2. **Verify Legitimacy**: Ensure it's not advertising/tracking
3. **Check Security**: No malware or suspicious behavior
4. **Cross-Platform Test**: Verify behavior across different DNS filtering platforms  
5. **Document Need**: Clear evidence of functional requirement

### 📝 Submission Format

```
Domain: example.com
Broken Functionality: User login system fails
Affected Blocklist: Energized Ultimate (or specify which from the 8-list stack)
Evidence: [Screenshot of broken login]
Testing Platform: Pi-hole/AdGuard/etc.
Blocklist Stack: Confirm you're using the complete 8-list combination
Security Check: Clean on VirusTotal
```

## 📊 Project Status

- **Target Blocklist Stack**: 8 specific comprehensive blocklists (see above)
- **Current Stage**: Single maintainer testing and validation against this exact stack
- **Platform Coverage**: Universal compatibility across all DNS filtering solutions
- **Domain Categories**: 6 major functionality areas
- **Vetting Process**: Manual testing against the complete blocklist combination
- **Community**: Growing - contributions welcome!

*Designed specifically for users running the complete aggressive blocklist stack listed above!*

## ⚠️ Security-First Approach

### Our Commitment
- **Security Never Compromised**: Functionality restoration without reducing protection
- **Conservative Allowlisting**: When in doubt, we exclude rather than include
- **Rigorous Testing**: Each domain tested across multiple DNS filtering platforms
- **Ongoing Monitoring**: Regular security reviews of all allowed domains

### Red Flags We Watch For
- Domains with mixed legitimate/tracking purposes
- Services with poor privacy practices
- Recently registered or suspicious domains
- Any domain with malware/phishing history

## 🔄 Maintenance Philosophy

### Maintenance Philosophy
- **Single-Point Testing**: Currently maintained and tested by project owner
- **Multi-Platform Validation**: Each domain tested across different DNS filtering solutions
- **Threat Intelligence**: Monitoring for any security issues with allowed domains
- **Community Growth**: Seeking additional testers and contributors

### Version Control
- **Semantic Versioning**: Clear tracking of changes
- **Change Documentation**: Every addition/removal explained
- **Rollback Capability**: Easy reversion if issues arise

## 🛠️ Testing Your Complete Setup

### Verify The Complete Blocklist Stack Is Working
```bash
# Test that all layers of blocking are active
nslookup doubleclick.net          # Should be blocked
nslookup googleadservices.com     # Should be blocked  
nslookup facebook.com/tr          # Should be blocked (tracking)
nslookup google-analytics.com     # Should be blocked
# All should return blocked/null responses
```

### Confirm Functionality Restoration  
```bash
# Test that essential services work despite aggressive blocking
nslookup login.microsoftonline.com  # Should work
nslookup checkout.paypal.com        # Should work
nslookup api.github.com             # Should work
# Should all return valid responses
```

### Complete Stack Validation
Only use this allowlist if you're running ALL 8 blocklists mentioned above. Using it with partial blocklist coverage may allow unwanted domains through.

## 📚 Complete Blocklist Stack Setup

### The Exact 8-List Combination
This allowlist is calibrated for this precise setup:

```
1. Energized Ultimate - https://energized.pro/ultimate/
2. NextDNS Ads & Trackers Blocklist - via NextDNS or equivalent  
3. AdGuard DNS Filter - https://github.com/AdguardTeam/AdguardFilters
4. OISD - https://oisd.nl/
5. 1Hosts (Xtra) - https://github.com/badmojr/1Hosts
6. hBlock - https://hblock.molinero.dev/
7. HaGeZi - Multi ULTIMATE - https://github.com/hagezi/dns-blocklists
8. Steven Black - https://github.com/StevenBlack/hosts
```

### Alternative Configurations
If you're not using this exact 8-list combination, this allowlist may:
- Allow domains that should be blocked (if you use fewer lists)
- Miss domains that need allowlisting (if you use different lists)

*For maximum effectiveness, deploy the complete stack above before applying this allowlist.*

## 📞 Community & Support

- **Security Issues**: Report immediately via GitHub issues
- **Functionality Problems**: Detailed reports with evidence
- **General Discussion**: Community discussions for strategy
- **Fast Response**: Critical functionality issues addressed within 24h

## 📄 License & Legal

This project is licensed under GPL-3.0. All domains are publicly researched and documented. No personal data is collected or processed.

## 🙏 Acknowledgments

- **DNS Security Community**: For developing comprehensive blocklists that enable maximum protection
- **Platform Developers**: Pi-hole, AdGuard Home, pfSense, OPNsense teams for excellent DNS filtering solutions  
- **Future Contributors**: Community members who will help expand testing and validation
- **Blocklist Maintainers**: Energized, Hagezi, 1Hosts, Steven Black, and others for their security work

---

**🔒 Maximum Security + 🚀 Full Functionality = Perfect Balance**

*Aggressive blocking doesn't have to mean broken websites. Block everything, then precisely restore what matters.*
