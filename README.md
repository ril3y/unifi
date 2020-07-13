# API Ubiquity UniFi Controller


```python 
c = controller.Controller(host="192.168.1.246")
c.username = "your_username"
c.password = "your_password"

print(c.logged_in) #False
c.connect()

print(c.logged_in) #True
clients = c.get_clients()

for client in clients:
  if "hostname" in client:
print("Hostname: " + client["hostname"])
print("OUI: " + client["oui"])
print("Network: " + client["network"])
```

There are other functions than get_clients().  

```
            authorize_guest()   disconnect()        get_clients()       get_users()         logged_in           reconnect_sta()     unblock_sta()
            block_sta()         forget_sta()        get_events()        get_wlan_conf()     password            site                username
            connect()           get_aps()           get_user_groups()   host                port                unauthorize_guest() version
            function(mac, minutes, up=None, down=None, mbytes=None, ap_mac=None)


