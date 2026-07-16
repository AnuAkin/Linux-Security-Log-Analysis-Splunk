# SPL Queries

## View all events

```spl
index=* sourcetype=*
```

## Top Source IP Addresses

```spl
index=* 
| stats count by src_ip
| sort -count
```

## Top Destination IP Addresses

```spl
index=*
| stats count by dest_ip
| sort -count
```

## Count Events

```spl
index=*
| stats count
```

## Search for FTP Connections

```spl
index=*
ftp
```

## Search by Source IP

```spl
index=*
src_ip="211.107.232.1"
```
