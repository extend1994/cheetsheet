## 網路查詢/修改指令

### 查詢/修改本機資訊

```shell
### if series ###
ifconfig [interface] [IP] [up|down|mtu|netmask|broadcast]
# 重啟網路服務
service networking restart # 方法1
/etc/init.d/networking restart # 方法2

ifup <interface>
ifdown <interface>

### route series ###
# -n no DNS name
# -ee show more details
route [-n|-ee]

# add, target 可以是 "default"
route add [-net|-host] target [netmask mask] [gw GW_IP] [dev Iface]

### ip series: 綜合 ifconfig & route ###
ip [-h[uman-readable] | -s[tatistics] | -c[olor] | -r[esolve]] \
   [link show | link set <device> up|down|name|address|mtu]    # link
   [address show | address add|del <IP/net> dev <device>]      # address
   [route show | route add|del <IP/net/default> [via GW] dev <device>] # route
```

### 查詢網域

```shell
dig <domain>
host -a <domain>
whois <domain>
```

### 封包監測 - `tcpdump`

- `-i <interface>`：指定監測的網卡
- `-c <count>`: 只抓指定數量的封包
- `-n`: 不查 IP 域名
- `-nn`: No port number
- `-v, -vv, -vvv`: 詳細資訊
- `-A`: ASCII
- `-x`: Hex
- `-X`: ASCII + Hex
- `-e`: L2 information
- `-tt`: timestamp
- `-tttt`: yyyy-mm-dd hh:mm:ss.ms
- `host <IP>`
- `net <IP with mask>`
