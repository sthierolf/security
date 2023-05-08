# Security

## CVE-2021-35061
Multiple Cross-site scripting (XSS) vulnerabilities in DRK Odenwaldkreis Testerfassung March-2021

Link: https://nvd.nist.gov/vuln/detail/CVE-2021-35061

## CVE-2021-35062
A Shell Metacharacter Injection vulnerability in result.php in DRK Odenwaldkreis Testerfassung March-2021

Link: https://nvd.nist.gov/vuln/detail/CVE-2021-35062

## sisyphus-win-10-telemetry.txt
Blocklist for Pi-Hole based on BSI SiSyPHuS Win 10 Telemetry data

Link: https://www.bsi.bund.de/EN/Topics/Cyber-Security/Recommendations/SiSyPHuS_Win10/AP4/SiSyPHuS_AP4_node.html

## Cisco-WLC-IDS
Cisco WLC IDS (Version 8.3) SNMP-Traps converted to yaml.

Blog post: https://www.thierolf.org/blog/2022/cisco-wireless-intrusion-detection-events-to-elastic-stack/

## bind9-rpz-blocklists
Blocklists based on https://github.com/blocklistproject/Lists and https://pgl.yoyo.org/adservers/serverlist.php in Bind9 RPZ (Response Policy Zones) format.

To include:

**named.conf.local**

  	zone "rpz.abuse.local" {
	    type master;
	    file "/etc/bind/db.rpz.abuse.local";
	  };
	 #...etc

**named.conf.options**

	response-policy {
		zone "rpz.abuse.local" policy drop;
	    	#...etc
  	};
  
