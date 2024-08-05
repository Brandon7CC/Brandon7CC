## Hi there 👋

My personal security blog is hosted on Notion at: [**swiftly-detecting.notion.site**](https://swiftly-detecting.notion.site/Swiftly-Detecting-Blog-c4000221c60d46ffb16c37b2425241e2).

---
## Some helpful links
* [**🌎 Endpoint Security client Survey 2023**](https://docs.google.com/spreadsheets/d/18lPTHjrgKsfLWknGpHg_bCasF1G7KRQlw0j6xs0oKx4/edit?gid=0#gid=0)
* [**Common macOS Data Sources**](https://github.com/redcanaryco/mac-monitor/wiki/2.-Common-Data-Sources)
  * [**Security Data Sources**](https://github.com/redcanaryco/mac-monitor/wiki/4.-Security-Data-Sources)
* **Endpoint Security Internals**
  * [**What makes Endpoint Security Special?**](https://github.com/redcanaryco/mac-monitor/wiki/5.-Endpoint-Security-Overview)
  * [**The Endpoint Security Daemon**](https://github.com/redcanaryco/mac-monitor/wiki/6.-Endpoint-Security-Daemon)
  * [**The Endpoint Security System DYLIB**](https://github.com/redcanaryco/mac-monitor/wiki/7.-Endpoint-Security-System-DYLIB)
  * [**The Endpoint Security DYLIB**](https://github.com/redcanaryco/mac-monitor/wiki/8.-Endpoint-Security-DYLIB)
  * [**Endpoint Security User Space Eventing**](https://github.com/redcanaryco/mac-monitor/wiki/9.-ES-User-Space-Eventing)

---

## Recent content

### 📝 ES Gatekeeper User Override

* **Published**: August 3, 2024  
* **Link**: https://swiftly-detecting.notion.site/ES-Gatekeeper-User-Override-31aea4ce3f804052bd4a81efaea76f6c  
>**Summary**: Apple has introduced a new Endpoint Security (ES) event in macOS 15 Sequoia called `ES_EVENT_TYPE_NOTIFY_GATEKEEPER_USER_OVERRIDE`, providing insight into Gatekeeper user overrides. This event, emitted by the `/usr/libexec/syspolicyd` daemon, does not enable authorization, but offers details like file type, path, CD hash, and SHA256 hash for files under 100MB. The event can be leveraged to detect instances where users bypass Gatekeeper restrictions, aiding in incident response and threat detection. Additionally, the `ExecPolicy` database's `policy_scan_cache` and `settings` table can be queried for the last override event by looking to the `lastGKOverride` value.


### 📝 Listing Connected ES Clients

* **Published**: August 2, 2024  
* **Link**: https://swiftly-detecting.notion.site/Listing-Connected-ES-Clients-fa6a47526b6942b9b5ab7339ebc17016
>**Summary**: It's possible to enumerate Endpoint Security (ES) clients (those who call into [`es_new_client(_:_:)`](https://developer.apple.com/documentation/endpointsecurity/3259700-es_new_client)) using the I/O Registry. The I/O Registry is a database representing the system's current "hardware" configuration and is organized into eight planes, with the `IOService` plane being of particular interest. The native `ioreg` utility can be used to query the `EndpointSecurityDriver` node, revealing connected ES clients as `EndpointSecurityExternalClient` objects. Additionally, Apple's `IORegistryExplorer.app` offers a graphical view of connected clients. 



<!--
**Brandon7CC/Brandon7CC** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
