# syslog_message_generator

Syslog Message Generator for lab

This project is just a syslog message generator for lab. The purpose is to send real syslog messages to a syslog servers without have the original devices that generate these syslogs.

First you must collect real syslog messages generated by real networking devices and collected by a real syslog server.

Save these syslogs into a text file named : **syslogs.txt**. The project contains an existing example that contains IPS syslog alerts ( web attack) from Cisco Secure Firewall

Then edit the **syslog_server_ip_address.txt** file

finally run the generator

    python 1-send_syslog_from_syslogs_text_file.py
    
This generator was created to be used in workshops in combination with the [syslog_server_for_XDR_demos](https://github.com/pcardotatgit/syslog_server_for_XDR_demos).

But it can be used for any other similar purposes.

It only sends messages ( every single line contained into syslogs.txt ) on UDP 514 port to the IP destination.

It doesn't modify anythin into the messages. That means that dates and times will be the one we have into the syslogs.txt file.

