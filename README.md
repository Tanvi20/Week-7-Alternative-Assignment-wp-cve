# Week-7-Alternative-Assignment-wp-cve

## 5 vulnerabilities using WordPress – Common Vulnerabilities and Exposure.

### 1) CVE-2018-5776
    
    WordPress before 4.9.2 had XSS in the Flash fallback files in MediaElement (under wp-includes/js/mediaelement). 
    Publish Date : 2018-  01-18, Last Update Date : 2018-02-01

    •	How the exploit was found
    According to CVE Details – The ultimate security vulnerability datasource – “An XSS vulnerability was discovered in the Flash fallback files in MediaElement, a library that is included with WordPress. 
    
    •	What the exploit does
    The CVE Details - The ultimate security vulnerability datasource described the type of this vulnerability as CWE-79 which means     Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting'). Furthermore, in this type of vulnerability, the software does not neutralize or incorrectly neutralizes user-controllable input before it is placed in output that is used as a web page that is served to other users.

    •	How it was fixed/patched
    It was figured that since the Flash files were no longer needed for most use cases, they had been removed from WordPress. WordPress 4.9.2, an update, was made available. This was regarded as a security and maintenance release for all versions since WordPress 3.7 and users were strongly encouraged to update their sites immediately. Also, MediaElement released a new version that contains a fix for the bug, and a WordPress plugin containing the fixed files was available in the plugin repository. Overall, 21 other bugs were fixed in WordPress 4.9.2, particularly of note were: JavaScript errors that prevented saving posts in Firefox, the previous taxonomy-agnostic behavior of get_category_link() and category_description() was restored, Switching themes (will now) attempt to restore previous widget assignments, even when there are no sidebars to map.

    Reference: 
    https://wordpress.org/news/2018/01/wordpress-4-9-2-security-and-maintenance-release/
    http://cwe.mitre.org/data/definitions/79.html
