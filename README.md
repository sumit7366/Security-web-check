<h1 align="center">Web-Check</h1>


<p align="center">
<img src="https://i.ibb.co/q1gZN2p/web-check-logo.png" width="96" /><br />
<b><i>Comprehensive, on-demand open source intelligence for any website</i></b>
<br />


</p>

---
<p align="center">
  <sup>Kindly supported by:</sup><br>
<a href="https://terminaltrove.com/?utm_campaign=github&utm_medium=referral&utm_content=web-check&utm_source=wcgh">
  <img src="https://i.ibb.co/8jrrcZ0/IMG-7210.jpg" width="300" alt="Terminal Trove">
  <br>
  <strong>The $HOME of all things in the terminal.</strong>
</a>
<br>
<a href="https://terminaltrove.com/newsletter?utm_campaign=github&utm_medium=referral&utm_content=web-check&utm_source=wcgh">
  <sub>Find your next CLI / TUI tool and more at Terminal Trove,</sub>
  <br>
  <sup>Get updates on new tools on our newsletter.</sup>
</a>
</p>

---



---

## About
Get an insight into the inner-workings of a given website: uncover potential attack vectors, analyse server architecture, view security configurations, and learn what technologies a site is using.

Currently the dashboard will show: IP info, SSL chain, DNS records, cookies, headers, domain info, search crawl rules, page map, server location, redirect ledger, open ports, traceroute, DNS security extensions, site performance, trackers, associated hostnames, carbon footprint. Stay tuned, as I'll add more soon!

The aim is to help you easily understand, optimize and secure your website.







### Features

<details open>
<summary><b>Click to expand / collapse section</b></summary>

<sup>**Note** _this list needs updating, many more jobs have been added since..._</sup>

The following section outlines the core features, and briefly explains why this data might be useful for you to know, as well as linking to further resources for learning more.

<details>
<summary><b>IP Info</b></summary>

###### Description
An IP address (Internet Protocol address) is a numerical label assigned to each device connected to a network / the internet. The IP associated with a given domain can be found by querying the Domain Name System (DNS) for the domain's A (address) record.

###### Use Cases
Finding the IP of a given server is the first step to conducting further investigations, as it allows us to probe the server for additional info. Including creating a detailed map of a target's network infrastructure, pinpointing the physical location of a server, identifying the hosting service, and even discovering other domains that are hosted on the same IP address.

###### Useful Links
- [Understanding IP Addresses](https://www.digitalocean.com/community/tutorials/understanding-ip-addresses-subnets-and-cidr-notation-for-networking)
- [IP Addresses - Wiki](https://en.wikipedia.org/wiki/IP_address)
- [RFC-791 Internet Protocol](https://tools.ietf.org/html/rfc791)
- [whatismyipaddress.com](https://whatismyipaddress.com/)

</details>
<details>
<summary><b>SSL Chain</b></summary>

<img width="300" src="https://i.ibb.co/kB7LsV1/wc-ssl.png" align="right" />

###### Description
SSL certificates are digital certificates that authenticate the identity of a website or server, enable secure encrypted communication (HTTPS), and establish trust between clients and servers. A valid SSL certificate is required for a website to be able to use the HTTPS protocol, and encrypt user + site data in transit. SSL certificates are issued by Certificate Authorities (CAs), which are trusted third parties that verify the identity and legitimacy of the certificate holder.

###### Use Cases
SSL certificates not only provide the assurance that data transmission to and from the website is secure, but they also provide valuable OSINT data. Information from an SSL certificate can include the issuing authority, the domain name, its validity period, and sometimes even organization details. This can be useful for verifying the authenticity of a website, understanding its security setup, or even for discovering associated subdomains or other services.

###### Useful Links
- [TLS - Wiki](https://en.wikipedia.org/wiki/Transport_Layer_Security)
- [What is SSL (via Cloudflare learning)](https://www.cloudflare.com/learning/ssl/what-is-ssl/)
- [RFC-8446 - TLS](https://tools.ietf.org/html/rfc8446)
- [SSL Checker](https://www.sslshopper.com/ssl-checker.html)

</details>
<details>
<summary><b>DNS Records</b></summary>

<img width="300" src="https://i.ibb.co/7Q1kMwM/wc-dns.png" align="right" />

###### Description
This task involves looking up the DNS records associated with a specific domain. DNS is a system that translates human-readable domain names into IP addresses that computers use to communicate. Various types of DNS records exist, including A (address), MX (mail exchange), NS (name server), CNAME (canonical name), and TXT (text), among others.

###### Use Cases
Extracting DNS records can provide a wealth of information in an OSINT investigation. For example, A and AAAA records can disclose IP addresses associated with a domain, potentially revealing the location of servers. MX records can give clues about a domain's email provider. TXT records are often used for various administrative purposes and can sometimes inadvertently leak internal information. Understanding a domain's DNS setup can also be useful in understanding how its online infrastructure is built and managed.

###### Useful Links
- [What are DNS records? (via Cloudflare learning)](https://www.cloudflare.com/learning/dns/dns-records/)
- [DNS Record Types](https://en.wikipedia.org/wiki/List_of_DNS_record_types)
- [RFC-1035 - DNS](https://tools.ietf.org/html/rfc1035)
- [DNS Lookup (via MxToolbox)](https://mxtoolbox.com/DNSLookup.aspx)

</details>
<details>
<summary><b>Cookies</b></summary>

<img width="300" src="https://i.ibb.co/TTQ6DtP/wc-cookies.png" align="right" />

###### Description
The Cookies task involves examining the HTTP cookies set by the target website. Cookies are small pieces of data stored on the user's computer by the web browser while browsing a website. They hold a modest amount of data specific to a particular client and website, such as site preferences, the state of the user's session, or tracking information.

###### Use Cases
Cookies can disclose information about how the website tracks and interacts with its users. For instance, session cookies can reveal how user sessions are managed, and tracking cookies can hint at what kind of tracking or analytics frameworks are being used. Additionally, examining cookie policies and practices can offer insights into the site's security settings and compliance with privacy regulations.

###### Useful Links
- [HTTP Cookie Docs (Mozilla)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
- [What are Cookies (via Cloudflare Learning)](https://www.cloudflare.com/learning/privacy/what-are-cookies/)
- [Testing for Cookie Attributes (OWASP)](https://owasp.org/www-project-web-security-testing-guide/v42/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes)
- [RFC-6265 - Coolies](https://tools.ietf.org/html/rfc6265)

</details>
<details>
<summary><b>Crawl Rules</b></summary>

<img width="300" src="https://i.ibb.co/KwQCjPf/wc-robots.png" align="right" />

###### Description
Robots.txt is a file found (usually) at the root of a domain, and is used to implement the Robots Exclusion Protocol (REP) to indicate which pages should be ignored by which crawlers and bots. It's good practice to avoid search engine crawlers from over-loading your site, but should not be used to keep pages out of search results (use the noindex meta tag or header instead).

###### Use Cases
It's often useful to check the robots.txt file during an investigation, as it can sometimes disclose the directories and pages that the site owner doesn't want to be indexed, potentially because they contain sensitive information, or reveal the existence of otherwise hidden or unlinked directories. Additionally, understanding crawl rules may offer insights into a website's SEO strategies.

###### Useful Links
- [Google Search Docs - Robots.txt](https://developers.google.com/search/docs/advanced/robots/intro)
- [Learn about robots.txt (via Moz.com)](https://moz.com/learn/seo/robotstxt)
- [RFC-9309 -  Robots Exclusion Protocol](https://datatracker.ietf.org/doc/rfc9309/)
- [Robots.txt - wiki](https://en.wikipedia.org/wiki/Robots_exclusion_standard)

</details>
<details>
<summary><b>Headers</b></summary>

<img width="300" src="https://i.ibb.co/t3xcwP1/wc-headers.png" align="right" />

###### Description
The Headers task involves extracting and interpreting the HTTP headers sent by the target website during the request-response cycle. HTTP headers are key-value pairs sent at the start of an HTTP response, or before the actual data. Headers contain important directives for how to handle the data being transferred, including cache policies, content types, encoding, server information, security policies, and more.

###### Use Cases
Analyzing HTTP headers can provide significant insights in an OSINT investigation. Headers can reveal specific server configurations, chosen technologies, caching directives, and various security settings. This information can help to determine a website's underlying technology stack, server-side security measures, potential vulnerabilities, and general operational practices.

###### Useful Links
- [HTTP Headers - Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)
- [RFC-7231 Section 7 - Headers](https://datatracker.ietf.org/doc/html/rfc7231#section-7)
- [List of header response fields](https://en.wikipedia.org/wiki/List_of_HTTP_header_fields)
- [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers/)

</details>
<details>
<summary><b>Quality Metrics</b></summary>

<img width="300" src="https://i.ibb.co/Kqg8rx7/wc-quality.png" align="right" />

###### Description
Using Lighthouse, the Quality Metrics task measures the performance, accessibility, best practices, and SEO of the target website. This returns a simple checklist of 100 core metrics, along with a score for each category, to gauge the overall quality of a given site.

###### Use Cases
Useful for assessing a site's technical health, SEO issues, identify vulnerabilities, and ensure compliance with standards.

###### Useful Links
- [Lighthouse Docs](https://developer.chrome.com/docs/lighthouse/)
- [Google Page Speed Tools](https://developers.google.com/speed)
- [W3 Accessibility Tools](https://www.w3.org/WAI/test-evaluate/)
- [Google Search Console](https://search.google.com/search-console)
- [SEO Checker](https://www.seobility.net/en/seocheck/)
- [PWA Builder](https://www.pwabuilder.com/)

</details>
<details>
<summary><b>Server Location</b></summary>

<img width="300" src="https://i.ibb.co/cXH2hfR/wc-location.png" align="right" />

###### Description
The Server Location task determines the physical location of the server hosting a given website based on its IP address. This is done by looking up the IP in a location database, which maps the IP to a lat + long of known data centers and ISPs. From the latitude and longitude, it's then possible to show additional contextual info, like a pin on the map, along with address, flag, time zone, currency, etc.

###### Use Cases
Knowing the server location is a good first step in better understanding a website. For site owners this aids in optimizing content delivery, ensuring compliance with data residency requirements, and identifying potential latency issues that may impact user experience in specific geographical regions. And for security researcher, assess the risk posed by specific regions or jurisdictions regarding cyber threats and regulations.

###### Useful Links
- [IP Locator](https://geobytes.com/iplocator/)
- [Internet Geolocation - Wiki](https://en.wikipedia.org/wiki/Internet_geolocation)

</details>
<details>
<summary><b>Associated Hosts</b></summary>

<img width="300" src="https://i.ibb.co/25j1sT7/wc-hosts.png" align="right" />

###### Description
This task involves identifying and listing all domains and subdomains (hostnames) that are associated with the website's primary domain. This process often involves DNS enumeration to discover any linked domains and hostnames, as well as looking at known DNS records.

###### Use Cases
During an investigation, understanding the full scope of a target's web presence is critical. Associated domains could lead to uncovering related projects, backup sites, development/test sites, or services linked to the main site. These can sometimes provide additional information or potential security vulnerabilities. A comprehensive list of associated domains and hostnames can also give an overview of the organization's structure and online footprint.

###### Useful Links
- [DNS Enumeration - Wiki](https://en.wikipedia.org/wiki/DNS_enumeration)
- [OWASP - Enumerate Applications on Webserver](https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/01-Information_Gathering/04-Enumerate_Applications_on_Webserver)
- [DNS Enumeration - DNS Dumpster](https://dnsdumpster.com/)
- [Subdomain Finder](https://subdomainfinder.c99.nl/)

</details>
<details>
<summary><b>Redirect Chain</b></summary>

<img width="300" src="https://i.ibb.co/hVVrmwh/wc-redirects.png" align="right" />

###### Description
This task traces the sequence of HTTP redirects that occur from the original URL to the final destination URL. An HTTP redirect is a response with a status code that advises the client to go to another URL. Redirects can occur for several reasons, such as URL normalization (directing to the www version of the site), enforcing HTTPS, URL shorteners, or forwarding users to a new site location.

###### Use Cases
Understanding the redirect chain can be useful for several reasons. From a security perspective, long or complicated redirect chains can be a sign of potential security risks, such as unencrypted redirects in the chain. Additionally, redirects can impact website performance and SEO, as each redirect introduces additional round-trip-time (RTT). For OSINT, understanding the redirect chain can help identify relationships between different domains or reveal the use of certain technologies or hosting providers.

###### Useful Links
- [HTTP Redirects - MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections)
- [URL Redirection - Wiki](https://en.wikipedia.org/wiki/URL_redirection)
- [301 Redirects explained](https://ahrefs.com/blog/301-redirects/)

</details>
<details>
<summary><b>TXT Records</b></summary>

<img width="300" src="https://i.ibb.co/wyt21QN/wc-txt-records.png" align="right" />

###### Description
TXT records are a type of DNS record that provides text information to sources outside your domain. They can be used for a variety of purposes, such as verifying domain ownership, ensuring email security, and even preventing unauthorized changes to your website.

###### Use Cases
The TXT records often reveal which external services and technologies are being used with a given domain. They may reveal details about the domain's email configuration, the use of specific services like Google Workspace or Microsoft 365, or security measures in place such as SPF and DKIM. Understanding these details can give an insight into the technologies used by the organization, their email security practices, and potential vulnerabilities.

###### Useful Links
- [TXT Records (via Cloudflare Learning)](https://www.cloudflare.com/learning/dns/dns-records/dns-txt-record/)
- [TXT Records - Wiki](https://en.wikipedia.org/wiki/TXT_record)
- [RFC-1464 - TXT Records](https://datatracker.ietf.org/doc/html/rfc1464)
- [TXT Record Lookup (via MxToolbox)](https://mxtoolbox.com/TXTLookup.aspx)

</details>
<details>
<summary><b>Server Status</b></summary>

<img width="300" src="https://i.ibb.co/V9CNLBK/wc-status.png" align="right" />

###### Description
Checks if a server is online and responding to requests.

###### Use Cases


###### Useful Links

</details>
<details>
<summary><b>Open Ports</b></summary>

<img width="300" src="https://i.ibb.co/F8D1hmf/wc-ports.png" align="right" />

###### Description
Open ports on a server are endpoints of communication which are available for establishing connections with clients. Each port corresponds to a specific service or protocol, such as HTTP (port 80), HTTPS (port 443), FTP (port 21), etc. The open ports on a server can be determined using techniques such as port scanning.

###### Use Cases
Knowing which ports are open on a server can provide information about the services running on that server, useful for understanding the potential vulnerabilities of the system, or for understanding the nature of the services the server is providing.

###### Useful Links
- [List of TCP & UDP Port Numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
- [NMAP - Port Scanning Basics](https://nmap.org/book/man-port-scanning-basics.html)

</details>
<details>
<summary><b>Traceroute</b></summary>

<img width="300" src="https://i.ibb.co/M59qgxP/wc-trace-route.png" align="right" />

###### Description
Traceroute is a network diagnostic tool used to track in real-time the pathway taken by a packet of information from one system to another. It records each hop along the route, providing details about the IPs of routers and the delay at each point.

###### Use Cases
In OSINT investigations, traceroute can provide insights about the routing paths and geography of the network infrastructure supporting a website or service. This can help to identify network bottlenecks, potential censorship or manipulation of network traffic, and give an overall sense of the network's structure and efficiency. Additionally, the IP addresses collected during the traceroute may provide additional points of inquiry for further OSINT investigation.

###### Useful Links
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })

</details>
<details>
<summary><b>Carbon Footprint</b></summary>

<img width="300" src="https://i.ibb.co/5v6fSyw/Screenshot-from-2023-07-29-19-07-50.png" align="right" />

###### Description
This task calculates the estimated carbon footprint of a website. It's based on the amount of data being transferred and processed, and the energy usage of the servers that host and deliver the website. The larger the website and the more complex its features, the higher its carbon footprint is likely to be.

###### Use Cases
From an OSINT perspective, understanding a website's carbon footprint doesn't directly provide insights into its internal workings or the organization behind it. However, it can still be valuable data in broader analyses, especially in contexts where environmental impact is a consideration. For example, it can be useful for activists, researchers, or ethical hackers who are interested in the sustainability of digital infrastructure, and who want to hold organizations accountable for their environmental impact.

###### Useful Links
- [WebsiteCarbon - Carbon Calculator](https://www.websitecarbon.com/)
- [The Green Web Foundation](https://www.thegreenwebfoundation.org/)
- [The Eco Friendly Web Alliance](https://ecofriendlyweb.org/)
- [Reset.org](https://en.reset.org/)
- [Your website is killing the planet - via Wired](https://www.wired.co.uk/article/internet-carbon-footprint)

</details>
<details>
<summary><b>Server Info</b></summary>

<img width="300" src="https://i.ibb.co/Mk1jx32/wc-server.png" align="right" />

###### Description
This task retrieves various pieces of information about the server hosting the target website. This can include the server type (e.g., Apache, Nginx), the hosting provider, the Autonomous System Number (ASN), and more. The information is usually obtained through a combination of IP address lookups and analysis of HTTP response headers.

###### Use Cases
In an OSINT context, server information can provide valuable clues about the organization behind a website. For instance, the choice of hosting provider could suggest the geographical region in which the organization operates, while the server type could hint at the technologies used by the organization. The ASN could also be used to find other domains hosted by the same organization.

###### Useful Links
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })

</details>
<details>
<summary><b>Whois Lookup</b></summary>

<img width="300" src="https://i.ibb.co/89WLp14/wc-domain.png" align="right" />

###### Description
This task retrieves Whois records for the target domain. Whois records are a rich source of information, including the name and contact information of the domain registrant, the domain's creation and expiration dates, the domain's nameservers, and more. The information is usually obtained through a query to a Whois database server.

###### Use Cases
In an OSINT context, Whois records can provide valuable clues about the entity behind a website. They can show when the domain was first registered and when it's set to expire, which could provide insights into the operational timeline of the entity. The contact information, though often redacted or anonymized, can sometimes lead to additional avenues of investigation. The nameservers could also be used to link together multiple domains owned by the same entity.

###### Useful Links
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })

</details>
<details>
<summary><b>Domain Info</b></summary>

<img width="300" src="https://i.ibb.co/89WLp14/wc-domain.png" align="right" />

###### Description
This task retrieves Whois records for the target domain. Whois records are a rich source of information, including the name and contact information of the domain registrant, the domain's creation and expiration dates, the domain's nameservers, and more. The information is usually obtained through a query to a Whois database server.

###### Use Cases
In an OSINT context, Whois records can provide valuable clues about the entity behind a website. They can show when the domain was first registered and when it's set to expire, which could provide insights into the operational timeline of the entity. The contact information, though often redacted or anonymized, can sometimes lead to additional avenues of investigation. The nameservers could also be used to link together multiple domains owned by the same entity.

###### Useful Links
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })

</details>
<details>
<summary><b>DNS Security Extensions</b></summary>

<img width="300" src="https://i.ibb.co/J54zVmQ/wc-dnssec.png" align="right" />

###### Description
Without DNSSEC, it's possible for MITM attackers to spoof records and lead users to phishing sites. This is because the DNS system includes no built-in methods to verify that the response to the request was not forged, or that any other part of the process wasn’t interrupted by an attacker. The DNS Security Extensions (DNSSEC) secures DNS lookups by signing your DNS records using public keys, so browsers can detect if the response has been tampered with. Another solution to this issue is DoH (DNS over HTTPS) and DoT (DNS over TLD).

###### Use Cases
DNSSEC information provides insight into an organization's level of cybersecurity maturity and potential vulnerabilities, particularly around DNS spoofing and cache poisoning. If no DNS secururity (DNSSEC, DoH, DoT, etc) is implemented, this may provide an entry point for an attacker.

###### Useful Links
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })

</details>
<details>
<summary><b>Site Features</b></summary>

<img width="300" src="https://i.ibb.co/gP4P6kp/wc-features.png" align="right" />

###### Description
Checks which core features are present on a site. If a feature as marked as dead, that means it's not being actively used at load time

###### Use Cases
This is useful to understand what a site is capable of, and what technologies to look for

###### Useful Links

</details>
<details>
<summary><b>HTTP Strict Transport Security</b></summary>

<img width="300" src="https://i.ibb.co/k253fq4/Screenshot-from-2023-07-17-20-10-52.png" align="right" />

###### Description
HTTP Strict Transport Security (HSTS) is a web security policy mechanism that helps protect websites against protocol downgrade attacks and cookie hijacking. A website can be included in the HSTS preload list by conforming to a set of requirements and then submitting itself to the list.

###### Use Cases
There are several reasons why it's important for a site to be HSTS enabled:
      1. User bookmarks or manually types http://example.com and is subject to a man-in-the-middle attacker
        HSTS automatically redirects HTTP requests to HTTPS for the target domain
      2. Web application that is intended to be purely HTTPS inadvertently contains HTTP links or serves content over HTTP
        HSTS automatically redirects HTTP requests to HTTPS for the target domain
      3. A man-in-the-middle attacker attempts to intercept traffic from a victim user using an invalid certificate and hopes the user will accept the bad certificate
        HSTS does not allow a user to override the invalid certificate message
        

###### Useful Links
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })
- [undefined](function link() { [native code] })

</details>
<details>
<summary><b>DNS Server</b></summary>

<img width="300" src="https://i.ibb.co/tKpL8F9/Screenshot-from-2023-08-12-15-43-12.png" align="right" />

###### Description
This check determines the DNS server(s) that the requested URL / IP resolves to. Also fires off a rudimentary check to see if the DNS server supports DoH, and weather it's vulnerable to DNS cache poisoning.

###### Use Cases


###### Useful Links

</details>
<details>
<summary><b>Tech Stack</b></summary>

<img width="300" src="https://i.ibb.co/bBQSQNz/Screenshot-from-2023-08-12-15-43-46.png" align="right" />

###### Description
Checks what technologies a site is built with. This is done by fetching and parsing the site, then comparing it against a bit list of RegEx maintained by Wappalyzer to identify the unique fingerprints that different technologies leave.

###### Use Cases
Identifying a website's tech stack aids in evaluating its security by exposing potential vulnerabilities, informs competitive analyses and development decisions, and can guide tailored marketing strategies. Ethical application of this knowledge is crucial to avoid harmful activities like data theft or unauthorized intrusion.

###### Useful Links
- [Wappalyzer fingerprints](https://github.com/wappalyzer/wappalyzer/tree/master/src/technologies)
- [BuiltWith - Check what tech a site is using](https://builtwith.com/)

</details>
<details>
<summary><b>Listed Pages</b></summary>

<img width="300" src="https://i.ibb.co/GtrCQYq/Screenshot-from-2023-07-21-12-28-38.png" align="right" />

###### Description
This job finds and parses a site's listed sitemap. This file lists public sub-pages on the site, which the author wishes to be crawled by search engines. Sitemaps help with SEO, but are also useful for seeing all a sites public content at a glance.

###### Use Cases
Understand the structure of a site's public-facing content, and for site-owners, check that you're site's sitemap is accessible, parsable and contains everything you wish it to.

###### Useful Links
- [Learn about Sitemaps](https://developers.google.com/search/docs/crawling-indexing/sitemaps/overview)
- [Sitemap XML spec](https://www.sitemaps.org/protocol.html)
- [Sitemap tutorial](https://www.conductor.com/academy/xml-sitemap/)

</details>
<details>
<summary><b>Security.txt</b></summary>

<img width="300" src="https://i.ibb.co/tq1FT5r/Screenshot-from-2023-07-24-20-31-21.png" align="right" />

###### Description
The security.txt file tells researchers how they can responsibly disclose any security issues found on your site. The standard was proposed in RFC 9116, and specifies that this file should include a point of contact (email address), as well as optionally other info, like a link to the security disclosure policy, PGP key, proffered language, policy expiry and more. The file should be located at the root of your domain, either at /security.txt or /.well-known/security.txt.

###### Use Cases
This is important, as without a defined point of contact a security researcher may be unable to report a critical security issue, or may use insecure or possibly public channels to do so. From an OSINT perspective, you may also glean info about a site including their posture on security, their CSAF provider, and meta data from the PGP public key.

###### Useful Links
- [securitytxt.org](https://securitytxt.org/)
- [RFC-9116 Proposal](https://datatracker.ietf.org/doc/html/rfc9116)
- [RFC-9116 History](https://datatracker.ietf.org/doc/rfc9116/)
- [Security.txt (Wikipedia)](https://en.wikipedia.org/wiki/Security.txt)
- [Example security.txt (Cloudflare)](https://www.cloudflare.com/.well-known/security.txt)
- [Tutorial for creating security.txt (Pieter Bakker)](https://pieterbakker.com/implementing-security-txt/)

</details>
<details>
<summary><b>Linked Pages</b></summary>

<img width="300" src="https://i.ibb.co/LtK14XR/Screenshot-from-2023-07-29-11-16-44.png" align="right" />

###### Description
Displays all internal and external links found on a site, identified by the href attributes attached to anchor elements.

###### Use Cases
For site owners, this is useful for diagnosing SEO issues, improving the site structure, understanding how content is inter-connected. External links can show partnerships, dependencies, and potential reputation risks. From a security standpoint, the outbound links can help identify any potential malicious or compromised sites the website is unknowingly linking to. Analyzing internal links can aid in understanding the site's structure and potentially uncover hidden or vulnerable pages which are not intended to be public. And for an OSINT investigator, it can aid in building a comprehensive understanding of the target, uncovering related entities, resources, or even potential hidden parts of the site.

###### Useful Links
- [W3C Link Checker](https://validator.w3.org/checklink)

</details>
<details>
<summary><b>Social Tags</b></summary>

<img width="300" src="https://i.ibb.co/4srTT1w/Screenshot-from-2023-07-29-11-15-27.png" align="right" />

###### Description
Websites can include certain meta tags, that tell search engines and social media platforms what info to display. This usually includes a title, description, thumbnail, keywords, author, social accounts, etc.

###### Use Cases
Adding this data to your site will boost SEO, and as an OSINT researcher it can be useful to understand how a given web app describes itself

###### Useful Links
- [SocialSharePreview.com](https://socialsharepreview.com/)
- [The guide to social meta tags](https://css-tricks.com/essential-meta-tags-social-media/)
- [Web.dev metadata tags](https://web.dev/learn/html/metadata/)
- [Open Graph Protocol](https://ogp.me/)
- [Twitter Cards](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards)
- [Facebook Open Graph](https://developers.facebook.com/docs/sharing/webmasters)

</details>
<details>
<summary><b>Email Configuration</b></summary>

<img width="300" src="https://i.ibb.co/yqhwx5G/Screenshot-from-2023-07-29-18-22-20.png" align="right" />

###### Description
DMARC (Domain-based Message Authentication, Reporting & Conformance): DMARC is an email authentication protocol that works with SPF and DKIM to prevent email spoofing and phishing. It allows domain owners to specify how to handle unauthenticated mail via a published policy in DNS, and provides a way for receiving mail servers to send feedback about emails' compliance to the sender. BIMI (Brand Indicators for Message Identification): BIMI is an emerging email standard that enables organizations to display a logo in their customers' email clients automatically. BIMI ties the logo to the domain's DMARC record, providing another level of visual assurance to recipients that the email is legitimate. DKIM (DomainKeys Identified Mail): DKIM is an email security standard designed to make sure that messages were not altered in transit between the sending and recipient servers. It uses digital signatures linked to the domain of the sender to verify the sender and ensure message integrity. SPF (Sender Policy Framework): SPF is an email authentication method designed to prevent email spoofing. It specifies which mail servers are authorized to send email on behalf of a domain by creating a DNS record. This helps protect against spam by providing a way for receiving mail servers to check that incoming mail from a domain comes from a host authorized by that domain's administrators.

###### Use Cases
This information is helpful for researchers as it helps assess a domain's email security posture, uncover potential vulnerabilities, and verify the legitimacy of emails for phishing detection. These details can also provide insight into the hosting environment, potential service providers, and the configuration patterns of a target organization, assisting in investigative efforts.

###### Useful Links
- [Intro to DMARC, DKIM, and SPF (via Cloudflare)](https://www.cloudflare.com/learning/email-security/dmarc-dkim-spf/)
- [EasyDMARC Domain Scanner](https://easydmarc.com/tools/domain-scanner)
- [MX Toolbox](https://mxtoolbox.com/)
- [RFC-7208 - SPF](https://datatracker.ietf.org/doc/html/rfc7208)
- [RFC-6376 - DKIM](https://datatracker.ietf.org/doc/html/rfc6376)
- [RFC-7489 - DMARC](https://datatracker.ietf.org/doc/html/rfc7489)
- [BIMI Group](https://bimigroup.org/)

</details>
<details>
<summary><b>Firewall Detection</b></summary>

<img width="300" src="https://i.ibb.co/MfcxQt2/Screenshot-from-2023-08-12-15-40-52.png" align="right" />

###### Description
A WAF or web application firewall helps protect web applications by filtering and monitoring HTTP traffic between a web application and the Internet. It typically protects web applications from attacks such as cross-site forgery, cross-site-scripting (XSS), file inclusion, and SQL injection, among others.

###### Use Cases
It's useful to understand if a site is using a WAF, and which firewall software / service it is using, as this provides an insight into the sites protection against several attack vectors, but also may reveal vulnerabilities in the firewall itself.

###### Useful Links
- [What is a WAF (via Cloudflare Learning)](https://www.cloudflare.com/learning/ddos/glossary/web-application-firewall-waf/)
- [OWASP - Web Application Firewalls](https://owasp.org/www-community/Web_Application_Firewall)
- [Web Application Firewall Best Practices](https://owasp.org/www-pdf-archive/Best_Practices_Guide_WAF_v104.en.pdf)
- [WAF - Wiki](https://en.wikipedia.org/wiki/Web_application_firewall)

</details>
<details>
<summary><b>HTTP Security Features</b></summary>

<img width="300" src="https://i.ibb.co/LP05HMV/Screenshot-from-2023-08-12-15-40-28.png" align="right" />

###### Description
Correctly configured security HTTP headers adds a layer of protection against common attacks to your site. The main headers to be aware of are: HTTP Strict Transport Security (HSTS): Enforces the use of HTTPS, mitigating man-in-the-middle attacks and protocol downgrade attempts. Content Security Policy (CSP): Constrains web page resources to prevent cross-site scripting and data injection attacks. X-Content-Type-Options: Prevents browsers from MIME-sniffing a response away from the declared content type, curbing MIME-type confusion attacks. X-Frame-Options: Protects users from clickjacking attacks by controlling whether a browser should render the page in a `<frame>`, `<iframe>`, `<embed>`, or `<object>`. 

###### Use Cases
Reviewing security headers is important, as it offers insights into a site's defensive posture and potential vulnerabilities, enabling proactive mitigation and ensuring compliance with security best practices.

###### Useful Links
- [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers/)
- [HTTP Header Cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Headers_Cheat_Sheet.html)
- [content-security-policy.com](https://content-security-policy.com/)
- [resourcepolicy.fyi](https://resourcepolicy.fyi/)
- [HTTP Security Headers](https://securityheaders.com/)
- [Mozilla Observatory](https://observatory.mozilla.org/)
- [CSP Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)
- [HSTS Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security)
- [X-Content-Type-Options Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options)
- [X-Frame-Options Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)
- [X-XSS-Protection Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection)

</details>
<details>
<summary><b>Archive History</b></summary>

<img width="300" src="https://i.ibb.co/nB9szT1/Screenshot-from-2023-08-14-22-31-16.png" align="right" />

###### Description
Fetches full history of archives from the Wayback machine

###### Use Cases
This is useful for understanding the history of a site, and how it has changed over time. It can also be useful for finding old versions of a site, or for finding content that has been removed.

###### Useful Links
- [Wayback Machine](https://archive.org/web/)

</details>
<details>
<summary><b>Global Ranking</b></summary>

<img width="300" src="https://i.ibb.co/nkbczgb/Screenshot-from-2023-08-14-22-02-40.png" align="right" />

###### Description
This check shows the global rank of the requested site. This is only accurate for websites which are in the top 100 million list. We're using data from the Tranco project (see below), which collates the top sites on the web from Umbrella, Majestic, Quantcast, the Chrome User Experience Report and Cloudflare Radar.

###### Use Cases
Knowing a websites overall global rank can be useful for understanding the scale of the site, and for comparing it to other sites. It can also be useful for understanding the relative popularity of a site, and for identifying potential trends.

###### Useful Links
- [Tranco List](https://tranco-list.eu/)
- [Tranco Research Paper](https://tranco-list.eu/assets/tranco-ndss19.pdf)

</details>
<details>
<summary><b>Block Detection</b></summary>

<img width="300" src="https://i.ibb.co/M5JSXbW/Screenshot-from-2023-08-26-12-12-43.png" align="right" />

###### Description
Checks access to the URL using 10+ of the most popular privacy, malware and parental control blocking DNS servers.

###### Use Cases


###### Useful Links
- [ThreatJammer Lists](https://threatjammer.com/osint-lists)

</details>
<details>
<summary><b>Malware & Phishing Detection</b></summary>

<img width="300" src="https://i.ibb.co/hYgy621/Screenshot-from-2023-08-26-12-07-47.png" align="right" />

###### Description
Checks if a site appears in several common malware and phishing lists, to determine it's threat level.

###### Use Cases
Knowing if a site is listed as a threat by any of these services can be useful for understanding the reputation of a site, and for identifying potential trends.

###### Useful Links
- [URLHaus](https://urlhaus-api.abuse.ch/)
- [PhishTank](https://www.phishtank.com/)

</details>
<details>
<summary><b>TLS Cipher Suites</b></summary>

<img width="300" src="https://i.ibb.co/6ydtH5R/Screenshot-from-2023-08-26-12-09-58.png" align="right" />

###### Description
These are combinations of cryptographic algorithms used by the server to establish a secure connection. It includes the key exchange algorithm, bulk encryption algorithm, MAC algorithm, and PRF (pseudorandom function).

###### Use Cases
This is important info to test for from a security perspective. Because a cipher suite is only as secure as the algorithms that it contains. If the version of encryption or authentication algorithm in a cipher suite have known vulnerabilities the cipher suite and TLS connection may then vulnerable to a downgrade or other attack

###### Useful Links
- [sslscan2 CLI](https://github.com/rbsec/sslscan)
- [ssl-enum-ciphers (NPMAP script)](https://nmap.org/nsedoc/scripts/ssl-enum-ciphers.html)

</details>
<details>
<summary><b>TLS Security Config</b></summary>

<img width="300" src="https://i.ibb.co/FmksZJt/Screenshot-from-2023-08-26-12-12-09.png" align="right" />

###### Description
This uses guidelines from Mozilla's TLS Observatory to check the security of the TLS configuration. It checks for bad configurations, which may leave the site vulnerable to attack, as well as giving advice on how to fix. It will also give suggestions around outdated and modern TLS configs

###### Use Cases
Understanding issues with a site's TLS configuration will help you address potential vulnerabilities, and ensure the site is using the latest and most secure TLS configuration.

###### Useful Links

</details>
<details>
<summary><b>TLS Handshake Simulation</b></summary>

<img width="300" src="https://i.ibb.co/F7qRZkh/Screenshot-from-2023-08-26-12-11-28.png" align="right" />

###### Description
This simulates how different clients (browsers, operating systems) would perform a TLS handshake with the server. It helps identify compatibility issues and insecure configurations.

###### Use Cases


###### Useful Links
- [TLS Handshakes (via Cloudflare Learning)](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/)
- [SSL Test (via SSL Labs)](https://www.ssllabs.com/ssltest/)

</details>
<details>
<summary><b>Screenshot</b></summary>

<img width="300" src="https://i.ibb.co/2F0x8kP/Screenshot-from-2023-07-29-18-34-48.png" align="right" />

###### Description
This check takes a screenshot of webpage that the requested URL / IP resolves to, and displays it.

###### Use Cases
This may be useful to see what a given website looks like, free of the constraints of your browser, IP, or location.


</details>

</details>



---

## Usage

### Deployment



### Deploying - 

Install the prerequisites listed in the [Developing](#developing) section, then run: 

```bash
git clone https://github.com/sumit7366/Security-web-check # Download the code from GitHub
cd Security-web-check                                        # Navigate into the project dir
yarn install                                        # Install the NPM dependencies
yarn build                                          # Build the app for production
yarn dev                                         # Start the app (API and GUI)
```

---

### Configuring

By default, no configuration is needed.

But there are some optional environmental variables that you can set to give you access to some additional checks, or to increase rate-limits for some checks that use external APIs.

**API Keys & Credentials**:

Key | Value
---|---
`GOOGLE_CLOUD_API_KEY` | A Google API key ([get here](https://cloud.google.com/api-gateway/docs/authenticate-api-keys)). This can be used to return quality metrics for a site
`REACT_APP_SHODAN_API_KEY` | A Shodan API key ([get here](https://account.shodan.io/)). This will show associated host names for a given domain
`REACT_APP_WHO_API_KEY` | A WhoAPI key ([get here](https://whoapi.com/)). This will show more comprehensive WhoIs records than the default job

<details>
  <summary><small>Full / Upcoming Vals</small></summary>
  
- `GOOGLE_CLOUD_API_KEY` - A Google API key ([get here](https://cloud.google.com/api-gateway/docs/authenticate-api-keys)). This can be used to return quality metrics for a site
- `REACT_APP_SHODAN_API_KEY` - A Shodan API key ([get here](https://account.shodan.io/)). This will show associated host names for a given domain
- `REACT_APP_WHO_API_KEY` - A WhoAPI key ([get here](https://whoapi.com/)). This will show more comprehensive WhoIs records than the default job
- `SECURITY_TRAILS_API_KEY` - A Security Trails API key ([get here](https://securitytrails.com/corp/api)). This will show org info associated with the IP
- `CLOUDMERSIVE_API_KEY` - API key for Cloudmersive ([get here](https://account.cloudmersive.com/)). This will show known threats associated with the IP
- `TRANCO_USERNAME` - A Tranco email ([get here](https://tranco-list.eu/)). This will show the rank of a site, based on traffic
- `TRANCO_API_KEY` - A Tranco API key ([get here](https://tranco-list.eu/)). This will show the rank of a site, based on traffic
- `URL_SCAN_API_KEY` - A URLScan API key ([get here](https://urlscan.io/)). This will fetch miscalanious info about a site
- `BUILT_WITH_API_KEY` - A BuiltWith API key ([get here](https://api.builtwith.com/)). This will show the main features of a site
- `TORRENT_IP_API_KEY` - A torrent API key ([get here](https://iknowwhatyoudownload.com/en/api/)). This will show torrents downloaded by an IP
  
</details>

**Configuration Settings**:

Key | Value
---|---
`PORT` | Port to serve the API, when running server.js (e.g. `3000`)
`API_ENABLE_RATE_LIMIT` | Enable rate-limiting for the /api endpoints (e.g. `true`)
`API_TIMEOUT_LIMIT` | The timeout limit for API requests, in milliseconds (e.g. `10000`)
`API_CORS_ORIGIN` | Enable CORS, by setting your allowed hostname(s) here (e.g. `example.com`)
`CHROME_PATH` | The path the Chromium executable (e.g. `/usr/bin/chromium`)
`DISABLE_GUI` | Disable the GUI, and only serve the API (e.g. `false`)
`REACT_APP_API_ENDPOINT` | The endpoint for the API, either local or remote (e.g. `/api`)

All values are optional.

You can add these as environmental variables. Either put them directly into an `.env` file in the projects root, or via the Netlify / Vercel UI, or by passing to the Docker container with the --env flag, or using your own environmental variable management system

Note that keys that are prefixed with `REACT_APP_` are used client-side, and as such they must be scoped correctly with minimum privileges, since may be made visible when intercepting browser <-> server network requests

---

### Developing

1. Clone the repo, `git clone git@https://github.com/sumit7366/Security-web-check`
2. Cd into it, `cd Security-web-check`
3. Install dependencies: `yarn`
4. Start the dev server, with `yarn dev`



---




### Dinosaurs are Awesome


# 🦖 DINOSAURS ARE AWESOME

```ansi
[1;32m
#============================#
#   D I N O S A U R S  0xAWE #
#============================#

         __
        / _)
 .-^^^-/ /
__/       /
<__.|_|-|_|

   __.-=-.       .-=-.__
.-'     `-._.-'     '-.
|  o     \__      __/ o |
|    .----' \    / '----. |
 \__.'      |  |        './
  '-._      |  |         _.'
      '-._ _|  |_     _.'
           '-._____.-'

[Access: GRANTED] ▓▓▓▓▓▓▓▓▓▓▓▓▓ 100%
[Protocol: D.I.N.O.] Initializing...

>> █ LOADING REX MODULE... █
>> █ BOOTING CARNIVORE CORE █
>> █ ACTIVATING CLAW FIREWALL █
>> █🦖 RUNNING JURASSIC MAINFRAME █

█▓▒░ 🦖 DINOSAURS ARE AWESOME ░▒▓█

#===============================#
#  Hack the past. Roar forward.#
#===============================#
[0m



                        . - ~ ~ ~ - .
      ..     _      .-~               ~-.
     //|     \ `..~                      `.
    || |      }  }              /       \  \
(\   \\ \~^..'                 |         }  \
 \`.-~  o      /       }       |        /    \
 (__          |       /        |       /      `.
  `- - ~ ~ -._|      /_ - ~ ~ ^|      /- _      `.
              |     /          |     /     ~-.     ~- _
              |_____|          |_____|         ~ - . _ _~_-_


