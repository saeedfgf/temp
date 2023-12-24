{
  "log": {
    "disabled": false,
    "level": "warn",
    "timestamp": true
  },
  "experimental": {
  },
  "dns": {
    "servers": [
      {
        "tag": "Internet-dns",
        "address": "94.140.14.14",
        "strategy": "ipv4_only",
        "detour": "Internet"
      },
      {
        "tag": "Best Latency-dns",
        "address": "94.140.14.14",
        "strategy": "ipv4_only",
        "detour": "Best Latency"
      },
      {
        "tag": "direct-dns",
        "address": "local",
        "strategy": "ipv4_only",
        "detour": "direct"
      },
      {
        "tag": "block-dns",
        "address": "rcode://success"
      }
    ],
    "rules": [
      {
        "domain_suffix": [
          ".arpa.",
          ".arpa"
        ],
        "server": "block-dns",
        "rewrite_ttl": 20
      },
      {
        "network": "udp",
        "port": 443,
        "server": "block-dns",
        "rewrite_ttl": 20
      },
      {
        "outbound": "Internet",
        "server": "Internet-dns",
        "rewrite_ttl": 20
      },
      {
        "outbound": "Best Latency",
        "server": "Best Latency-dns",
        "rewrite_ttl": 20
      }
    ],
    "reverse_mapping": true,
    "strategy": "ipv4_only",
    "independent_cache": true,
    "disable_cache": true
  },
  "inbounds": [
    {
      "type": "tun",
      "tag": "tun-in",
      "interface_name": "tun0",
      "inet4_address": "172.19.0.1/30",
      "mtu": 9000,
      "auto_route": true,
      "strict_route": true,
      "stack": "system",
      "endpoint_independent_nat": true,
      "sniff": true
    },
    {
      "listen": "0.0.0.0",
      "listen_port": 2080,
      "sniff": true,
      "tag": "mixed-in",
      "type": "mixed"
    }
  ],
  "outbounds": [
    {
      "type": "selector",
      "tag": "Internet",
      "outbounds": [
        "Best Latency",
        "🌐 @Ln2ray",
        "🌐 @Ln2ray 2",
        "🌐 @Ln2ray 3",
        "🌐 @Ln2ray 4",
        "🌐 @Ln2ray 5",
        "🌐 @Ln2ray 6",
        "🌐 @Ln2ray 7",
        "🌐 @Ln2ray 8",
        "🌐 @Ln2ray 9",
        "🌐 @Ln2ray 10"
      ]
    },
    {
      "type": "urltest",
      "tag": "Best Latency",
      "outbounds": [
        "🌐 @Ln2ray",
        "🌐 @Ln2ray 2",
        "🌐 @Ln2ray 3",
        "🌐 @Ln2ray 4",
        "🌐 @Ln2ray 5",
        "🌐 @Ln2ray 6",
        "🌐 @Ln2ray 7",
        "🌐 @Ln2ray 8",
        "🌐 @Ln2ray 9",
        "🌐 @Ln2ray 10"
      ],
      "url": "http://www.google.com/generate_204",
      "interval": "30s"
    },
    {
      "tag": "🌐 @Ln2ray",
      "type": "vless",
      "server": "104.16.237.74",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 2",
      "type": "vless",
      "server": "104.16.110.215",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 3",
      "type": "vless",
      "server": "104.25.233.226",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 4",
      "type": "vless",
      "server": "190.93.244.51",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 5",
      "type": "vless",
      "server": "190.93.247.14",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 6",
      "type": "vless",
      "server": "172.66.209.117",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 7",
      "type": "vless",
      "server": "188.114.97.1",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 8",
      "type": "vless",
      "server": "103.21.244.5",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 9",
      "type": "vless",
      "server": "104.27.91.235",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "tag": "🌐 @Ln2ray 10",
      "type": "vless",
      "server": "188.114.97.143",
      "server_port": 443,
      "uuid": "6e34f2c5-6c71-4010-c292-10d05ef4a9a2",
      "flow": "",
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
      "download_url": "https://github.com/bootmortis/iran-hosted-domains/releases/latest/download/iran-geosite.db",
      "download_detour": "Best Latency"
    },
    "rules": [
    {
        "geosite": "all",
        "outbound": "direct"
      },
      {
        "geosite": "ads",
        "outbound": "block"
      },
      {
        "domain_suffix": [".ir"],
        "outbound": "direct"
      },
      {
        "outbound": "dns-out",
        "port": [
          53
        ]
      }
    ]
  }
}