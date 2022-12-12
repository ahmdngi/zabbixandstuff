#### How To Integrate Zabbix with MS Teams to get instants Messages with triggers.

MS Teams: 
we need to setup a channel and a connector which will be used later
 - Create a new channel 
 - go for connectors 
 - use the search bar to find > Incoming Webhook 
 - Press configure and generate the webhook and save it > This will be Placeholder 2 in the yaml file.


Zabbix:
 - Download and Edit [This File](https://github.com/ahmdngi/zabbixandstuff/blob/main/zbx_import_mediatypes.yaml)
 - we hace 3 placeholders
    - Placeholder 1 is zabbix version 
    - Placeholder 2 from above
    - Placeholder 3 is the same as Placeholder 2 or the first part of it 
 - go to Administration > Media Types > press the right left button <Import> and import the yaml file.
 - go to General > Macros > add a macro for {$ZABBIX.URL} with value of the UI link.
 - go to Users > Media > add > 
     - Type > MS Teams 
     - Send To > link to the channel (NOT THE WEBHOOK LINK)
 - go to Configuration > Actions > Trigger Actions > Create Action for the top right
     - Action > Create Conditions based on your preferences(If you have mulitple conditions use OR as a type of calcualtion).
     - Operations > press add under operations >
        - add an admin user > Send to users
