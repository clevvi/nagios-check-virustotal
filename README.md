# nagios-check-virustotal Nagios plugin to check a URL against VirusTotal's API

Features
--------

This plugin checks a URL against VirusTotal's API, which in turn checks against many popular security vendors.

VirusTotal's API is rate limited. If the rate limit is exceeded, a 204 HTTP response will be returned. The plugin will in turn return an UNKNOWN reponse to Nagios.

The URL must be supplied as complete, including the protocol, eg: 'https://www.clevvi.com.au'


Requirements
------------

Python 2.7


Configuration
-----

The configuration variables at the top of the script determine:

* VirusTotal API key (api_key)
* Nagios "critical" threshold (threshold_critical)
* Nagios "warning" threshold (threshold_warn)

The Phishtank API key can be obtained for free at: https://www.virustotal.com/#/join-us.


Usage
-----

Syntax:

	check_virustotal '<url>'

`<url>` is the complete URL to check, including protocol
