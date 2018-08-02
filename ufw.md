# UFW Firewall

## General

### Status (List all current rules)

```
sudo ufw status verbose
```

### Enable

```
sudo ufw enable
```

### Disable

```
sudo ufw disable
```

### Reset UFW rules

```
sudo ufw reset
```

## Block

### IP-address

```
sudo ufw deny from 15.15.15.51
```

### Deny outgoing from port

```
sudo ufw deny out 25
```

### Deny to Network interface

```
sudo ufw deny in on eth0 from 15.15.15.51
```

## Allow

### IP-address

```
sudo ufw allow from 15.15.15.15
```

### Subnet to specific port

```
sudo ufw allow from 15.15.15.0/24  to any port 22
```

### Service

```
sudo ufw allow https
```

### Port

```
sudo ufw allow 25
```
