# Web Infrastructure Design

Four designs for `www.foobar.com`, progressing from a single server to
separate, redundant service tiers. All diagrams and explanations are in English.

## Deliverables

Each extensionless answer file contains exactly one public PNG screenshot
URL. GitHub hosts the images in this repository; the SVG files are editable
sources. The PNGs are browser screenshots of those original SVG diagrams.

| Task | Answer file | Diagram | Explanation |
| --- | --- | --- | --- |
| 0. Simple web stack | [Answer](./0-simple_web_stack) | [PNG](./diagrams/0-simple_web_stack.png) | [Notes](./notes/0-simple_web_stack.md) |
| 1. Distributed web infrastructure | [Answer](./1-distributed_web_infrastructure) | [PNG](./diagrams/1-distributed_web_infrastructure.png) | [Notes](./notes/1-distributed_web_infrastructure.md) |
| 2. Secured and monitored web infrastructure | [Answer](./2-secured_and_monitored_web_infrastructure) | [PNG](./diagrams/2-secured_and_monitored_web_infrastructure.png) | [Notes](./notes/2-secured_and_monitored_web_infrastructure.md) |
| 3. Scale up | [Answer](./3-scale_up) | [PNG](./diagrams/3-scale_up.png) | [Notes](./notes/3-scale_up.md) |

Task 0 follows the supplied current assignment. Tasks 1–3 were checked against
public copies of the project requirements. These copies list task 3 as advanced;
the current intranet's classification was not independently verified. See
[references and scope](./REFERENCES.md).

## Reading the diagrams

- Dashed large rectangles mark host boundaries; smaller boxes are services.
- Blue arrows carry web requests. Responses return along the reverse path.
- Purple arrows show database access; dashed purple arrows show replicated data.
- Green arrows carry monitoring data; they are separate from website traffic.
- DNS resolves the hostname before the browser connects. It does not forward HTTP.

Tasks 1 and 2 use exactly three infrastructure hosts: one load balancer and two
web/application/database hosts. The monitoring service in task 2 is external.
Task 3 deliberately uses eight dedicated hosts to retain redundant pairs while
separating roles; this is more than the minimum one-host addition.

The domain and addresses are assignment values used only in drawings. No live
DNS records, certificates, firewalls, servers or monitoring services were deployed.

## Vocabulary for the oral review

| Term | Meaning |
| --- | --- |
| DNS | Domain Name System; resolves names through records such as A and CNAME. |
| A record | Associates a hostname with an IPv4 address. |
| CNAME | Makes one DNS name an alias of another name; not used for `www` in task 0. |
| LAMP | Linux, Apache, MySQL and PHP/Perl/Python. These drawings use Nginx, not Apache, so they are not literally a LAMP stack. |
| SPOF | Single point of failure: one component whose failure can interrupt a required service. |
| QPS | Queries per second; here, the number of web requests handled per second. |
| HTTPS / TLS | HTTP protected by Transport Layer Security. The assignment says SSL; modern connections use TLS. |
| HA | High availability; redundancy plus health detection and a working failover path. |
| VIP / VRRP | Virtual IP address / Virtual Router Redundancy Protocol; used for the load-balancer failover design. |

## Whiteboard preparation

Start with a user entering the URL. Draw DNS, then follow one request through
the infrastructure and trace its response back. Explain each new component,
identify remaining failure points, and stop when the requested scope is covered.

For a 30-minute rehearsal, allow roughly 5 minutes for task 0, 8 for task 1,
10 for task 2 and 7 for task 3. Practise recreating the drawings without notes.
Written explanations and images do not replace the required live review.

## Verification and submission

The PNGs were rendered and visually inspected. Text boundaries, local links,
answer-file formats and LF line endings were checked. These checks validate
the deliverables, not a running infrastructure or a Holberton manual review.

Use the four links in [SUBMISSION.md](./SUBMISSION.md) for the intranet URL boxes.
The task links do not submit themselves or mark tasks green automatically.
