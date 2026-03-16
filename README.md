# Observations of a [TCL 55C7K](https://www.tcl.com/global/en/tvs/55c7k) on the network

## Notes

Prior to testing all unnecessary apps on the TV have been disabled or
uninstalled as far as possible, but some of them can't be. TODO: Detailed list
Camera and Microphone access has been disabled in Android for all apps. Location
services have been declined. To all privacy settings that where shown, the
opt-out option was used, if possible. TODO: Detailed list, of privacy questions.

A second approach was tested, to use [mitmproxy](https://www.mitmproxy.org/) to
further inspect the https traffic, but Android TV does not directly support
installing TLS certificates. TODO: Maybe via adb or root? And even with an
installed certificate, apps don't usually trust user installed certificates,
unless patched to do so. See: <https://android-developers.googleblog.com/2016/07/changes-to-trusted-certificate.html> and <https://docs.mitmproxy.org/stable/howto/install-system-trusted-ca-android/>

## Files

- **reboot_and_five_mins_idle.pcapng** contains the (cleaned-up) network traffic of
  the TV during a reboot followed by a five minute idle period.

- **dnsqueries.txt** (and cleanded-up version) extracted from the network traffic, all DNS queries the TV made

- **pihole.png** settings to block dodgy domains in pihole

- **ai_report.md/html** Hallucinations from GeminiAI when told to research the dodgy domains

## See also

- <https://sick.codes/extraordinary-vulnerabilities-discovered-in-tcl-android-tvs-now-worlds-3rd-largest-tv-manufacturer/>
- <https://zahidrasheed.medium.com/charles-proxy-with-androidtv-fedc863e7039>
