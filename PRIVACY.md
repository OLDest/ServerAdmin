# ServerAdmin Privacy Policy

Effective date: 8 October 2026. Applies to ServerAdmin, its optional ServerAdminJobService and Pageant broker, and the DevOpsTasks integration used by ServerAdmin.

Canonical policy: [English](https://serveradmin.su/en/privacy/) · [Русский](https://serveradmin.su/privacy/).

## Scope and responsibility

ServerAdmin is a Windows administration application. It processes the connection settings and operational data needed to manage the servers and virtual machines you select. Your organization controls those systems, the application installation, its Web users, and the destinations you configure. Only administer systems and collect information you are authorized to access; screenshots, command results and files can contain other people's personal or confidential information.

## Connection settings and credentials

ServerAdmin stores server names, host addresses, ports, account names, server groups, VM settings and selected connection options locally. Saved passwords use Windows Data Protection API (DPAPI). Depending on the credential and workflow, protection is tied to the current Windows user or to the computer; machine-scope credentials support service and shared configuration workflows. Legacy password formats may be read and migrated. DPAPI is not protection against every process or administrator with access to the same Windows account or computer. Protect the installation, configuration, backups and Windows accounts.

With SSH keys, private keys stay in Pageant. ServerAdmin and its local Pageant broker request identities and signatures and retain the selected public-key identifier and, where configured, the Windows user SID. ServerAdmin does not upload Pageant private keys to the publisher. SSH passwords and fallback Proxmox/PBS API credentials are used to authenticate to the configured systems. RDP can use Windows Credential Manager; browser, RDP and VNC components may maintain their own credentials, cookies or connection history under their own settings.

## Remote access and DevOpsTasks

ServerAdmin connects to configured Proxmox/PBS and Windows systems through SSH, HTTPS, RDP, VNC, browser views and the DevOpsTasks agent. Connection identifiers, authentication exchanges, commands, responses and console traffic pass to the systems involved. DevOpsTasks can execute PowerShell and desktop-session commands, transfer selected files, and return screenshots and system information such as hardware, processes, services and network details. Command output and transferred or captured content are returned to the requesting ServerAdmin installation or its authorized Web client and may be saved locally. A command or script you run may itself contact other destinations. Publisher services are not a relay for ordinary server-management traffic.

## Local operational records and the Web interface

Local data can include configuration, server and VM caches, recent actions, task results and errors, monitoring CSV files, incident snapshots, Web users and audit records, logs, downloaded files, screenshots, system-information exports, diagnostic bundles and configuration backups. These records can contain system names, addresses, user names, command text or output and file paths. Some histories are bounded by record count; CSV files, exported files and backups can remain until you remove them. There is no single automatic deletion period for all local data. Review diagnostic bundles and exports before sharing them.

The optional Web interface exposes permitted data and actions to users you configure. Restrict listening addresses, ports, network access and Web roles, and use appropriate transport protection. A browser that connects directly to Proxmox or another service sends data to that service according to its own settings and policy.

## Monitoring webhooks

When you configure a webhook, monitoring can send a normalized JSON snapshot to that URL. It can include server/VM identifiers, addresses, status, resource measurements and incident details. Delivery failures may be recorded locally. The destination operator controls subsequent access, use and retention. Configure only trusted URLs, check what the destination receives, and remove or disable the webhook to stop future deliveries. Removing a webhook does not erase data already sent.

## Background service and user controls

If installed and enabled, ServerAdminJobService can keep the Web interface, scheduled checks and background jobs running after the desktop application closes. SSH access uses the configured user-session Pageant broker. Closing the desktop window alone does not stop a running service. Use the application's service controls or Windows service management to stop/remove it. You can remove saved connections and credentials, restrict Web users, disable monitoring/history or webhooks, cancel supported tasks, unload Pageant keys, and stop the relevant applications and services. Removing ServerAdmin does not by itself uninstall a remote DevOpsTasks agent, undo remote commands, delete third-party records or erase your exports/backups. Manage those separately.

For local deletion, first stop the desktop application and service, then remove the records you no longer need from the installation's configuration/data/log/history folders and any separately selected export, screenshot, download or backup locations. Clear associated Windows Credential Manager entries and browser data separately where applicable. Retain configuration only if you intend to reuse it; running processes can recreate records. Secure deletion and removal from backups require your own storage/backup procedures.

## Telemetry, updates and third-party services

ServerAdmin has no built-in publisher usage-analytics, advertising or automatic operational-data/crash-report telemetry. It does contact the official download host to check update information and download packages; the integrated DevOpsTasks agent has its own update checks. These requests disclose normal HTTP connection information, such as the requesting IP address, to the hosting service and may appear in its access logs. This is separate from management traffic and from optional webhooks. No support bundle is automatically submitted by ServerAdmin.

Windows, WebView2, Pageant, Proxmox/PBS, RDP/VNC/SSH clients, your identity providers, configured webhook recipients, hosting/mail services and GitHub/WinGet may independently process information under their own configuration and policies. Their retention and deletion are not controlled by ServerAdmin. Follow the policies of services you choose and the rules of your organization.

## This website and support

The serveradmin.su website and download hosting can log IP addresses, request URLs, times, browser/user-agent and referrer information for operation and security. The site's visitor counter sends a SHA-256 hash derived from the visitor IP address to CounterAPI (counterapi.com); an IP hash is a persistent identifier, not a guarantee of anonymity. Download clicks update a local aggregate counter. CAPTCHA and rate-limit state use short-lived records, including IP-derived hashes; cleanup is periodic and is not guaranteed to occur at an exact deadline.

The contact form sends the name, email, message, selected language and requesting IP address to ServerAdmin support through a mail service. Support correspondence may remain in the support mailbox and its backups as needed to handle the request; no fixed automatic mailbox deletion period is promised. Do not send passwords, private keys, tokens or unnecessary personal data. Contact support to ask about information you submitted or request its deletion; records held by your own installation, administrators or third parties must be handled with those parties.

## Security, contact and changes

Network administration, remote command execution and screen/file access carry security risks. Encryption and access controls do not guarantee complete confidentiality on a compromised endpoint or against an authorized administrator. Keep Windows and dependencies updated, review permissions and destination addresses, and protect local and remote backups. This policy describes data flows; it does not guarantee the behavior of arbitrary commands, scripts or third-party components.

Contact: [ServerAdmin support](https://serveradmin.su/en/#contact). For vulnerabilities, follow [the security reporting policy](https://github.com/OLDest/ServerAdmin/blob/main/SECURITY.md). Future policy revisions will be published at the canonical policy URLs with an updated effective date.
