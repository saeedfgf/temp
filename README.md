

    "auto_detect_interface": true,
    "override_android_vpn": true,
    "final": "Internet",
    "geoip": {
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
