This plugin can check the status of Uninterruptible Power Supply (UPS) using SNMP v1 queries.

The check_snmp_ups is written in Bash and is distributed under the GPLv2 license. This plugin have been created by Yoann LAMY.

Usage: ./check_snmp_ups -H xxx.xxx.xxx.xxx -C public -t battery

-H ADDRESS
Name or IP address of host (default: 127.0.0.1)
-C STRING
Community name for the host's SNMP agent (default: public)
-t STRING
Different status (battery, charge, power, source, temperature) (default: battery)
-w INTEGER
Warning battery level in percent and UPS Warning temperature level in degres celsius (default: 0)
-c INTEGER
Critical battery level in percent and UPS Critical temperature level in degres celsius (default: 0)
-h
Print this help screen
-V
Print version and license information

This plugin uses 'snmpget' and 'snmpwalk' commands included with the NET-SNMP package.
This plugin support performance data output (charge, power, temperature).

Examples :

./check_snmp_ups -H xxx.xxx.xxx.xxx -C public -t battery
./check_snmp_ups -H xxx.xxx.xxx.xxx -C public -t charge -w 70 -c 30
./check_snmp_ups -H xxx.xxx.xxx.xxx -C public -t power -w 0 -c 0
./check_snmp_ups -H xxx.xxx.xxx.xxx -C public -t source
./check_snmp_ups -H xxx.xxx.xxx.xxx -C public -t temperature -w 0 -c 0

This nagios plugins comes with ABSOLUTELY NO WARRANTY.

You may redistribute copies of the plugins under the terms of the GNU General Public License v2. 
