# AdBlock DNS Filters
去广告合并规则，每8个小时更新一次。  
个人收藏了不少广告过滤规则，但是每次往新设备添加的时候很是头疼，于是写了这个项目，定时自动获取各规则源更新，生成合并规则库。

## 说明
1. 定时从上游各规则源获取更新，合并去重。
2. 使用国内、国外各 3 组 DNS 服务，分别对上游各规则源拦截的域名进行解析，去除已无法解析的域名。（上游各规则源中存在大量已无法解析的域名，无需加入拦截规则）
3. 本项目仅对上游规则进行合并、去重、去除无效域名，不做任何修改。如发现误拦截情况，可临时添加放行规则（如 `@@||www.example.com^$important`），并向上游规则反馈。

## 订阅链接
1. 规则x’为规则x的 Lite 版，仅针对国内域名拦截，体积较小（如添加完整规则报错数量限制，请尝试 Lite 规则）
2. 已对 jsdelivr(加速链接1) 缓存进行主动刷新，但仍存在一定刷新延时
3. AdGuard 等浏览器插件使用规则1 + 规则2（规则2为规则1的补充，仅适用浏览器插件）

| 规则 | 原始链接 | 加速链接1 | 加速链接2 | 加速链接3 | 适配说明 |
|:-|:-|:-|:-|:-|:-|
| 规则1 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockdns.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdns.txt) | AdGuard、AdGuard Home 等 |
| 规则1' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnslite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockdnslite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnslite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnslite.txt) | AdGuard、AdGuard Home 等 |
| 规则2 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilters.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockfilters.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilters.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilters.txt) | AdGuard 等 |
| 规则2' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilterslite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockfilterslite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilterslite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockfilterslite.txt) | AdGuard 等 |
| 规则3 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdomain.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockdomain.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdomain.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdomain.txt) | InviZible Pro、personalDNSfilter |
| 规则3' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdomainlite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockdomainlite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdomainlite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdomainlite.txt) | InviZible Pro、personalDNSfilter |
| 规则4 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnsmasq.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockdnsmasq.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnsmasq.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnsmasq.txt) | DNSMasq |
| 规则4' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnsmasqlite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockdnsmasqlite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnsmasqlite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockdnsmasqlite.txt) | DNSMasq |
| 规则5 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksmartdns.conf) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblocksmartdns.conf) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksmartdns.conf) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksmartdns.conf) | SmartDNS |
| 规则5' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksmartdnslite.conf) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblocksmartdnslite.conf) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksmartdnslite.conf) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksmartdnslite.conf) | SmartDNS |
| 规则6 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockclash.list) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockclash.list) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockclash.list) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockclash.list) | Shadowrocket |
| 规则6' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockclashlite.list) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockclashlite.list) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockclashlite.list) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockclashlite.list) | Shadowrocket |
| 规则7 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockqx.conf) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockqx.conf) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockqx.conf) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockqx.conf) | QuantumultX |
| 规则7' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockqxlite.conf) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockqxlite.conf) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockqxlite.conf) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockqxlite.conf) | QuantumultX |
| 规则8 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomo.yaml) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockmihomo.yaml) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomo.yaml) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomo.yaml) | Clash Meta(Mihomo) yaml |
| 规则8' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomolite.yaml) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockmihomolite.yaml) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomolite.yaml) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomolite.yaml) | Clash Meta(Mihomo) yaml |
| 规则9 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomo.mrs) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockmihomo.mrs) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomo.mrs) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomo.mrs) | Clash Meta(Mihomo) mrs |
| 规则9' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomolite.mrs) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockmihomolite.mrs) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomolite.mrs) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockmihomolite.mrs) | Clash Meta(Mihomo) mrs |
| 规则10 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockhosts.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockhosts.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockhosts.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockhosts.txt) | Hosts |
| 规则10' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockhostslite.txt) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockhostslite.txt) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockhostslite.txt) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockhostslite.txt) | Hosts |
| 规则11 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingbox.json) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblocksingbox.json) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingbox.json) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingbox.json) | sing-box 1.12.x json |
| 规则11' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingboxlite.json) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblocksingboxlite.json) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingboxlite.json) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingboxlite.json) | sing-box 1.12.x json |
| 规则12 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingbox.srs) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblocksingbox.srs) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingbox.srs) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingbox.srs) | sing-box 1.12.x srs |
| 规则12' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingboxlite.srs) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblocksingboxlite.srs) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingboxlite.srs) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblocksingboxlite.srs) | sing-box 1.12.x srs |
| 规则13 | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockloon.list) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockloon.list) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockloon.list) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockloon.list) | Loon |
| 规则13' | [原始链接](https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockloonlite.list) | [加速链接1](https://gcore.jsdelivr.net/gh/217heidai/adblockfilters@main/rules/adblockloonlite.list) | [加速链接2](https://github.boki.moe/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockloonlite.list) | [加速链接3](https://ghfast.top/https://raw.githubusercontent.com/217heidai/adblockfilters/main/rules/adblockloonlite.list) | Loon |

## 上游规则源

| 规则 | 类型 | 原始链接 | 加速链接1 | 加速链接2 | 加速链接3 | 更新日期 |
|:-|:-|:-|:-|:-|:-|:-|
| AdGuard Base filter | filter | [原始链接](https://raw.githubusercontent.com/AdguardTeam/FiltersRegistry/master/filters/filter_2_Base/filter.txt) | | | | 2026/05/30 |
| AdGuard Chinese filter | filter | [原始链接](https://raw.githubusercontent.com/AdguardTeam/FiltersRegistry/master/filters/filter_224_Chinese/filter.txt) | | | | 2026/05/30 |
| AdGuard Mobile Ads filter | filter | [原始链接](https://raw.githubusercontent.com/AdguardTeam/AdguardFilters/master/MobileFilter/sections/adservers.txt) | | | | 2026/05/30 |
| AdGuard DNS filter | filter | [原始链接](https://adguardteam.github.io/AdGuardSDNSFilter/Filters/filter.txt) | | | | 2026/05/30 |
| EasyList | filter | [原始链接](https://easylist-downloads.adblockplus.org/easylist.txt) | | | | 2026/05/30 |
| EasyList China | filter | [原始链接](https://easylist-downloads.adblockplus.org/easylistchina.txt) | | | | 2026/05/30 |
| EasyPrivacy | filter | [原始链接](https://easylist-downloads.adblockplus.org/easyprivacy.txt) | | | | 2026/05/30 |
| CJX's Annoyance List | filter | [原始链接](https://raw.githubusercontent.com/cjx82630/cjxlist/master/cjx-annoyance.txt) | | | | 2026/05/30 |
| xinggsf rule | filter | [原始链接](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/rule.txt) | | | | 2026/05/30 |
| xinggsf mv | filter | [原始链接](https://raw.githubusercontent.com/xinggsf/Adblock-Plus-Rule/master/mv.txt) | | | | 2026/05/30 |
| jiekouAD | filter | [原始链接](https://raw.githubusercontent.com/damengzhu/banad/main/jiekouAD.txt) | | | | 2026/05/30 |
| anti-AD | filter | [原始链接](https://anti-ad.net/adguard.txt) | | | | 2026/05/30 |
| ADgk | filter | [原始链接](https://raw.githubusercontent.com/banbendalao/ADgk/master/ADgk.txt) | | | | 2026/05/30 |
| 大圣净化 Purple | filter | [原始链接](https://raw.githubusercontent.com/hhui64/url-filter/master/all/purple.txt) | | | | 2026/05/30 |
| AdRules DNS List | dns | [原始链接](https://raw.githubusercontent.com/Cats-Team/AdRules/main/dns.txt) | | | | 2026/05/30 |
| Hagezi Light | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/light.txt) | | | | 2026/05/30 |
| Hagezi Pro | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/pro.txt) | | | | 2026/05/30 |
| Hagezi Ultimate | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/ultimate.txt) | | | | 2026/05/30 |
| Hagezi Threat Intelligence | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/tif.txt) | | | | 2026/05/30 |
| Hagezi Anti-Piracy | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/piracy.txt) | | | | 2026/05/30 |
| Hagezi Xiaomi | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/native.xiaomi.txt) | | | | 2026/05/30 |
| Hagezi Apple | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/native.apple.txt) | | | | 2026/05/30 |
| Hagezi Huawei | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/native.huawei.txt) | | | | 2026/05/30 |
| Hagezi TikTok | dns | [原始链接](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/native.tiktok.txt) | | | | 2026/05/30 |
| 1Hosts Lite | dns | [原始链接](https://raw.githubusercontent.com/badmojr/1Hosts/master/Lite/adblock.txt) | | | | 2026/05/30 |
| OISD Full | dns | [原始链接](https://abp.oisd.nl/) | | | | 2026/05/30 |
| AWAvenue Ads Rule | dns | [原始链接](https://raw.githubusercontent.com/TG-Twilight/AWAvenue-Ads-Rule/main/AWAvenue-Ads-Rule.txt) | | | | 2026/05/30 |
| Hblock | dns | [原始链接](https://hblock.molinero.dev/hosts_adblock.txt) | | | | 2026/05/30 |
| BlockListProject Ads | dns | [原始链接](https://raw.githubusercontent.com/blocklistproject/Lists/master/ads.txt) | | | | 2026/05/30 |
| BlockListProject Tracking | dns | [原始链接](https://raw.githubusercontent.com/blocklistproject/Lists/master/tracking.txt) | | | | 2026/05/30 |
| Peter Lowe | dns | [原始链接](https://pgl.yoyo.org/adservers/serverlist.php?hostformat=adblockplus&mimetype=plaintext) | | | | 2026/05/30 |
| AdAway | host | [原始链接](https://adaway.org/hosts.txt) | | | | 2026/05/30 |
| GoodbyeAds | host | [原始链接](https://raw.githubusercontent.com/jerryn70/GoodbyeAds/master/Hosts/GoodbyeAds.txt) | | | | 2026/05/30 |
| 1024_hosts | host | [原始链接](https://raw.githubusercontent.com/Goooler/1024_hosts/master/hosts) | | | | 2026/05/30 |

## Star History
[![Star History Chart](https://api.star-history.com/svg?repos=217heidai/adblockfilters&type=Date)](https://star-history.com/#217heidai/adblockfilters&Date)

## 以下是广告
感兴趣的可以看下，DartNode 免费 VPS, [点击申请](https://dartnode.com?aff=PudgyBurrito637)
[![Powered by DartNode](https://dartnode.com/branding/DN-Open-Source-sm.png)](https://dartnode.com "Powered by DartNode - Free VPS for Open Source")
