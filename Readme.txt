=== Universal AdsBlock & VPN Detector ===
Contributors: ilblogdicristiangallo  
Tags: adblock detection, vpn awareness, dns filtering, privacy education, security overlay, diagnostic plugin  
Requires at least: 5.0  
Tested up to: 6.8.3  
Requires PHP: 7.4  
Stable tag: 1.0  
License: GPLv2 or later  
License URI: https://www.gnu.org/licenses/gpl-2.0.html  

== Description ==  
Universal AdsBlock & VPN Detector is a modular WordPress plugin designed for educational and diagnostic purposes. It detects AdBlock usage, filtered DNS, and VPN connections via known ASNs in real time. The plugin displays a customizable informational overlay to promote transparency and user awareness. It is fully compatible with all themes, devices, and mobile browsers.  

This plugin does not block access, collect personal data, or interfere with navigation. It is built for privacy-respecting environments and complies with WordPress coding standards and GDPR principles.  

== Requirements ==  
* WordPress 5.0 or higher  
* PHP 7.4+, 8.0+, 8.2  
* Compatible with both Classic and Gutenberg editors  

== Theme Compatibility ==  
* Does not rely on theme-specific hooks  
* Injects the overlay via `wp_footer`, present in all well-structured themes  

== Installation ==  
1. Log in to your WordPress admin panel  
2. Navigate to Plugins → Add New → Upload Plugin  
3. Select the `.zip` file of Universal AdsBlock & VPN Detector  
4. Click “Install Now”, then “Activate”  
5. Go to Settings → AdsBlock Detector to configure options  

== Frequently Asked Questions ==  
= Does this plugin block access? =  
No. It displays an informational overlay. It does not prevent navigation or restrict access.  

= Is this plugin safe to use? =  
Yes. It follows WordPress coding standards, does not collect or transmit user data, and is fully compatible with privacy-first environments.  

== Detection Methods ==  
This plugin performs non-invasive client-side detection using three modular techniques:  

1. **AdBlock Detection**  
   - Uses a 1px invisible bait element (`.adsbox`) with a background image (`/ads.jpg`)  
   - If the bait is hidden or removed by browser extensions, AdBlock is considered active  

2. **Google Ads Script Blocking**  
   - Attempts to load `adsbygoogle.js` from Google Ads CDN  
   - If the script fails to load (`onerror`), it indicates ad script blocking  

3. **VPN Detection via ASN**  
   - Fetches public ASN data from `https://ipinfo.io/json`  
   - Compares the `org` field against a curated list of known VPN ASN identifiers  
   - The list is maintained in the plugin’s modular core (`inc/vpn-check.php`) and includes providers offering DNS filtering, tracker blocking, or ad suppression  
   - No IP or personal data is stored or transmitted  

All detection logic is executed client-side via JavaScript and does not interfere with navigation or collect user data. The overlay is purely informational and can be disabled or customized via the plugin settings.  

== Security and Transparency ==  
Universal AdsBlock & VPN Detector is built with full respect for user privacy and platform integrity.  

The plugin:  
* Does not block access or restrict navigation  
* Does not track users or fingerprint devices  
* Does not inject third-party scripts or load external resources from unverified domains  
* Uses only standard WordPress APIs and adheres to WordPress.org coding guidelines  
* Is fully compatible with GDPR and privacy-first environments  

Its purpose is strictly educational and diagnostic, designed to raise awareness about content filtering and network-level privacy tools. The overlay is informational only and can be disabled or customized by the site administrator.  

This plugin has been tested for compatibility with major caching, security, and accessibility plugins. It does not interfere with SEO, page indexing, or crawler visibility.  

For full source code and contribution history, visit: https://github.com/ilblogdicristiangallo/Universal-Adsblock-Detector  

== Changelog ==  
= 1.0 =  
* Initial release with AdBlock, DNS filter, and VPN detection via ASN  

== Upgrade Notice ==  
Stable release. No breaking changes.
