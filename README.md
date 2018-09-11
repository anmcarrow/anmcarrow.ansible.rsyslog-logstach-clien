Tiny Ansible role for reconfigure the Rsyslog service
and enable remote Rsyslog-logging to the  Logstash/ELK service.

### Additional info:
Of course, before the run of this role to your host, you need to configure appropriate Logstash pipline.


#### For example:

```json
input {
  udp {
    port => 10514
    codec => "json"
    type => "rsyslog"
  }
}

input {
  tcp {
    port => 10514
    codec => "json"
    type => "rsyslog"
  }
}
```

**Tested on:** Debian 9 and CentOS 7

- Author: am (mb@mcrrw.me)
- Licence: MIT
