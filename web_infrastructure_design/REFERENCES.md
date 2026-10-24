# References and scope

Research date: October 23, 2026.

## Assignment scope

Task 0, its exact repository path and its current requirements were supplied
directly by the user. They take precedence over historical copies.

The public [Holberton project requirements copy](https://github.com/fchavonet/holbertonschool-system_engineering-devops/blob/main/web_infrastructure_design/README.md)
lists the same four task filenames used here. An archived
[ALX/Holberton assignment copy](https://www.scribd.com/document/679974812/Project-0x09-Web-infrastructure-design-ALX-Africa-Intranet)
corroborates the sequence: simple, distributed, secured/monitored, then scale up.
The latter uses a historical `0x09-` directory; this repository uses the user's
current `web_infrastructure_design` directory instead.

These references establish task scope, not a private checker result. Current
private intranet pages were not accessible during research. No other student's
diagram or solution was copied; the diagrams and explanations here were created
for this submission. Task 3's eight-host count is an explicit design choice
that exceeds the minimum server addition and preserves redundancy across tiers.

## Technical sources

| Topic | Primary documentation |
| --- | --- |
| DNS A records | [Cloudflare](https://www.cloudflare.com/learning/dns/dns-records/dns-a-record/) |
| Static content, proxying, graceful reload | [Nginx beginner's guide](https://nginx.org/en/docs/beginners_guide.html) |
| Round-robin backend selection | [HAProxy backends](https://www.haproxy.com/documentation/haproxy-configuration-tutorials/proxying-essentials/configuration-basics/backends/) |
| MySQL source/replica behavior | [MySQL replication implementation](https://dev.mysql.com/doc/refman/8.0/en/replication-implementation.html) |
| Firewall purpose | [Cloudflare](https://www.cloudflare.com/learning/security/what-is-a-firewall/) |
| HTTPS | [MDN glossary](https://developer.mozilla.org/en-US/docs/Glossary/HTTPS) |
| Frontend and backend TLS | [HAProxy TLS documentation](https://www.haproxy.com/documentation/haproxy-configuration-tutorials/security/ssl-tls/basics-enable-tls/) |
| Monitoring collection | [Sumo Logic installed collectors](https://www.sumologic.com/help/docs/send-data/installed-collectors/) |
| Web request counter | [Nginx stub status](https://nginx.org/en/docs/http/ngx_http_stub_status_module.html) |
| Active-passive VRRP clustering | [HAProxy clustering overview](https://cdn.haproxy.com/assets/content-library/datasheets/haproxy-enterprise.pdf) |

This is a design project. The public images document diagrams, not screenshots
of provisioned servers or proof of a completed manual assessment.
