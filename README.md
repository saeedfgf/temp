

      "packet_encoding": "xudp",
      "multiplex": {
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      },
      "tls": {
        "enabled": true,
        "server_name": "current.ircp.online",
        "insecure": true,
        "disable_sni": false
      },
      "transport": {
        "type": "ws",
        "path": "/",
        "headers": {
          "Host": "current.ircp.online"
        },
        "max_early_data": 0,
      "packet_encoding": "xudp",
      "multiplex": {
        "enabled": false,
        "protocol": "smux",
        "max_streams": 32
      },
      "tls": {
        "enabled": true,
        "server_name": "current.ircp.online",
        "insecure": true,
        "disable_sni": false
      },
      "transport": {
        "type": "ws",
        "path": "/",
        "headers": {
          "Host": "current.ircp.online"
        },
        "max_early_data": 0,
        "early_data_header_name": "Sec-WebSocket-Protocol"
      },
      "domain_strategy": "ipv4_only"
    },
    {
      "type": "direct",
      "tag": "direct"
    },
    {
      "type": "block",
      "tag": "block"
    },
    {
      "type": "dns",
      "tag": "dns-out"
    }
  ],
  "route": {
    "auto_detect_interface": true,
    "override_android_vpn": true,
    "final": "Internet",
    "geoip": {
      "download_url": "https://github.com/malikshi/sing-box-geo/releases/latest/download/geoip.db",
      "download_detour": "Best Latency"
    },
    "geosite": {
      "path": "iran-geosite.db",
      "download_url": "https://github.co        "geosite": "ads",
        "outbound": "block"
      },
      {
        "domain_suffix": [".ir"],
        "outbound": "direct"

