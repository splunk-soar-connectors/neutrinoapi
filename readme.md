[comment]: # "Auto-generated SOAR connector documentation"
# Neutrino API

Publisher: Zachery Turpen  
Connector Version: 1\.0\.1  
Product Vendor: Neutrino  
Product Name: Neutrino API  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.251  

Detect potentially malicious or dangerous IP addresses by integrating with Neutrino API


Use this app for identifying malicious hosts, anonymous proxies, Tor Nodes, botnets, spammers and
more.  
Block, filter and flag traffic to help reduce attacks on your networks and software.  
Blocklists are generated from 3 primary source categories:  
1) System of automated bots, crawlers and honeypots which continuously collect data from across the
Internet.  
2) Firewall Aggregation from thousands of commercial and open-source security appliances.  
3) Open Data collected from many public sources of IP related data including public blocklists,
blacklists, malware/botnet trackers and various security intelligence feeds.


### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Neutrino API asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**api\_user** |  required  | string | Api User
**api\_key** |  required  | password | Api Key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[lookup ip](#action-lookup-ip) - Check for the presence of an IP in a threat intelligence feed  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'lookup ip'
Check for the presence of an IP in a threat intelligence feed

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP to lookup | string |  `ip` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip | string |  `ip` 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 
action\_result\.data\.\*\.is\-exploit\-bot | boolean | 
action\_result\.data\.\*\.is\-listed | boolean | 
action\_result\.data\.\*\.is\-spider | boolean | 
action\_result\.data\.\*\.is\-vpn | boolean | 
action\_result\.data\.\*\.last\-seen | numeric | 
action\_result\.data\.\*\.is\-malware | boolean | 
action\_result\.data\.\*\.is\-spyware | boolean | 
action\_result\.data\.\*\.is\-spam\-bot | boolean | 
action\_result\.data\.\*\.is\-dshield | boolean | 
action\_result\.data\.\*\.is\-hijacked | boolean | 
action\_result\.data\.\*\.list\-count | numeric | 
action\_result\.data\.\*\.is\-bot | boolean | 
action\_result\.data\.\*\.is\-proxy | boolean | 
action\_result\.data\.\*\.is\-tor | boolean | 
action\_result\.summary\.Listed on Blocklist | boolean | 