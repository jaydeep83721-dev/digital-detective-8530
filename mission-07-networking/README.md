# Mission 7 — How Computers Communicate

## 1. Task / Objective

The objective of Mission 7 is to understand how computer networks work, explore important networking concepts, test network connectivity, perform a DNS lookup, and explain how a browser communicates with a web server.

## 2. Work Completed

### Task 7.1 — Explain Network Concepts

I studied eight fundamental networking concepts and identified their practical applications.

| Concept | Explanation | Example |
|---|---|---|
| LAN (Local Area Network) | Connects devices within a small geographical area. | Computers connected in a college laboratory. |
| MAN (Metropolitan Area Network) | Connects networks across a city or large campus area. | A city-wide municipal network. |
| WAN (Wide Area Network) | Connects networks across large geographical distances. | The Internet. |
| DNS (Domain Name System) | Resolves domain names into IP addresses. | Looking up `example.com`. |
| Router | Connects networks and forwards packets between them. | A home Wi-Fi router connecting a local network to the Internet. |
| Protocol | Defines rules for communication between devices. | HTTPS for secure website communication. |
| Packet Switching | Divides data into packets that are transmitted across a network. | Loading a webpage over the Internet. |
| Client-Server | A client requests information or services, and a server provides a response. | A browser requesting a webpage from a web server. |

### Task 7.2 — Observe Network Information

I used the macOS Terminal to test connectivity to a public example website and perform a DNS lookup.

#### Activity 1 — Connectivity Test

Command used:

```bash
ping -c 4 example.com
```

**Observed results:**

| Measurement | Result |
|---|---|
| Packets transmitted | 4 |
| Packets received | 4 |
| Packet loss | 0.0% |
| Minimum round-trip time | 5.782 ms |
| Average round-trip time | 6.791 ms |
| Maximum round-trip time | 7.669 ms |

**Observation:**

All four packets received responses, with no packet loss.

The average round-trip time was 6.791 milliseconds.

This demonstrated successful ICMP connectivity to the destination during the test.

#### Activity 2 — DNS Lookup

Command used:

```bash
nslookup example.com
```

The DNS lookup successfully returned two IPv4 addresses for `example.com`.

The response was marked as non-authoritative, meaning it was supplied by a DNS resolver rather than directly by the authoritative DNS server.

Personal network information has been omitted from this report.

#### Questions and Answers

**Q1. What does a connectivity test help you check?**

A connectivity test helps determine whether a computer can reach another device or network destination. The ping command sends test packets and measures responses, packet loss, and round-trip time.

**Q2. What information does a DNS lookup display?**

A DNS lookup can display the IP addresses associated with a domain name. My lookup returned two IPv4 addresses for the example domain.

**Q3. What is the role of DNS when entering a website name in a browser?**

DNS translates a domain name into an IP address so the browser can identify the destination and establish a network connection.

### Task 7.3 — What Happens When You Open a Website?

I studied the process that occurs when a browser opens a webpage.

**Six main steps:**

1. **Enter a website address:** The user enters a URL such as `https://example.com` into the browser, which acts as the client.

2. **DNS resolution:** The browser obtains an IP address associated with the website's domain name using DNS, unless an appropriate result is already cached.

3. **Establish a connection:** The computer communicates through its network connection and routers to reach the destination server. Depending on the connection, protocols such as TCP, TLS, or QUIC may be involved.

4. **Send an HTTP request:** The browser sends an HTTPS request to the server asking for the webpage.

5. **Receive the server's response:** The server processes the request and sends a response containing webpage data, such as HTML.

6. **Display the webpage:** The browser processes the response, retrieves additional resources when necessary, and renders the webpage for the user.

This activity helped me understand how clients, servers, DNS, routers, and network protocols work together.

## 3. Commands / Tools Used

| Command / Tool | Purpose |
|---|---|
| macOS Terminal | Execute networking commands. |
| `ping` | Test network reachability using ICMP packets. |
| `-c 4` | Limit ping to four packets. |
| `nslookup` | Retrieve DNS information for a domain. |
| Web browser | Access websites as a network client. |
| Visual Studio Code | Write and organise mission documentation. |

## 4. My Understanding

I learned that computer networks allow devices to communicate and share information.

LAN, MAN, and WAN describe networks covering different geographical areas.

DNS helps computers find the network addresses associated with website names.

I also learned that routers forward packets between networks and that communication protocols establish rules for exchanging data.

The connectivity and DNS tests helped me understand how networking concepts are used in practice.

## 5. Difficulties Faced

No major difficulties were encountered during the connectivity test or DNS lookup.

## 6. How I Resolved Them

Not applicable. Both networking commands completed successfully.

## 7. Evidence / Files

The Mission 7 folder contains:

```text
mission-07-networking/
└── README.md
```

The README includes:

- Eight networking concepts with examples.
- Actual ping observations and round-trip times.
- Privacy-safe DNS lookup findings.
- Answers to the three networking questions.
- A six-step explanation of how a website loads.

## 8. Commit Details

**Commit message:** `Explain networking concepts and website communication`

**Repository:** https://github.com/jaydeep83721-dev/digital-detective-8530

**Commit:** `0708b31` — Explain networking concepts and website communication.

**Push status:** Successfully pushed to GitHub.
