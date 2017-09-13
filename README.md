# iw-zabbix-templates
Zabbix 3.4 template for Infinet devices. Current version is only for InfiLINK, InfiMAN (R5000) devices.

## For whome
If you are using Zabbix 3.4 for your network monitoring, this templates could be useful for you.
Templates contains a list of MIB objects, graphs, triggers and screens. 

## Get started

### Requirements
Zabbix 3.4 installed.

### Get
1. Download template file from this repo: `template_Infinet_Net_R5000_SNMPv2.xml`
2. Open your zabbix site in browser with "Admin" access.
3. Go to "Configuration" -&gt; "Templates"
4. Click "Import" button in top right coner
5. Select checkboxes for "Update existing" and "Create new" next items: 
Templates, Template screens, Template linkage, Applications, Items, Discovery rules, Triggers, Graphs, Screens, Value mappings
    You'll get something like this: ![Zabbix template import screenshot](https://cloud.mail.ru/public/8RTr/T5U7SRwwU)
    **Attention! Do not** select any checkbox in "Delete missing" column.
6. Click "Choose file" and find template files which you've downloaded in 1 step.
7. Click "Import button"
8. Add InfiLINK/InfiMAN devices, configure SNMP (with macro {$SNMP_COMMUNITY}) and link it with "Template Net Infinet R5000 SNMPv2" template. 

### Content
The template file consists from:
* Top level template "Template Net Infinet R5000 SNMPv2" 
* Two modules "Template Module Infinet AQUARADIO-MIB SNMPv2" and "Template Module Infinet AQUAMINT-MIB SNMPv2"
* Few value maps with "AQUARADIO-MIB::" and "AQUAMINT-MIB::" prefixes
* "Template Net Infinet R5000 SNMPv2" links with "Generic SNMPv2" too, so I'll get standard graphs for network interfaces
It provides links discovery, graphs, triggers, host screens.<br>
**Note**: to see the "host screen", configure "automatic" inventory for the device. Then go to "Inventory" -&gt; "Hosts", click "your device", click "Screens".

## Help
Your feedback is highly appreciated. You can write here <https://github.com/Mir-ina/iw-zabbix-templates/issues> 

## TODO
1. Templates for XG
