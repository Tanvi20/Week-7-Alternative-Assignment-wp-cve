# Week-7-Alternative-Assignment-wp-cve

## 5 vulnerabilities using WordPress – Common Vulnerabilities and Exposure.

### 1) CVE-2018-5776
    
    WordPress before 4.9.2 had XSS in the Flash fallback files in MediaElement (under wp-includes/js/mediaelement). Publish Date : 2018-  01-18, Last Update Date : 2018-02-01

    •	How the exploit was found
    According to CVE Details – The ultimate security vulnerability datasource – “An XSS vulnerability was discovered in the Flash fallback files in MediaElement, a library that is included with WordPress. 
    
    •	What the exploit does
    The CVE Details - The ultimate security vulnerability datasource described the type of this vulnerability as CWE-79 which means Improper Neutralization of Input During Web Page Generation ('Cross-site Scripting'). Furthermore, in this type of vulnerability, the software does not neutralize or incorrectly neutralizes user-controllable input before it is placed in output that is used as a web page that is served to other users.

    •	How it was fixed/patched
    It was figured that since the Flash files were no longer needed for most use cases, they had been removed from WordPress. WordPress 4.9.2, an update, was made available. This was regarded as a security and maintenance release for all versions since WordPress 3.7 and users were strongly encouraged to update their sites immediately. Also, MediaElement released a new version that contains a fix for the bug, and a WordPress plugin containing the fixed files was available in the plugin repository. Overall, 21 other bugs were fixed in WordPress 4.9.2, particularly of note were: JavaScript errors that prevented saving posts in Firefox, the previous taxonomy-agnostic behavior of get_category_link() and category_description() was restored, Switching themes (will now) attempt to restore previous widget assignments, even when there are no sidebars to map.

    Reference: 
    https://wordpress.org/news/2018/01/wordpress-4-9-2-security-and-maintenance-release/
    http://cwe.mitre.org/data/definitions/79.html


### 2) CVE-2018-10102

    Before WordPress 4.9.5, the version string was not escaped in the get_the_generator function, and could lead to XSS in a generator tag. 
    Publish Date : 2018-04-16, Last Update Date : 2018-05-18

    •	How the exploit was found
    The weakness was disclosed 04/16/2018. This vulnerability is known as CVE-2018-10102. A vulnerability classified as problematic was found in WordPress up to 4.9.4. Affected by this vulnerability is the function get_the_generator. The manipulation with an unknown input leads to a cross site scripting vulnerability.

    •	What the exploit does
    WordPress is eventually prone to a cross-site scripting vulnerability. According to Security Focus, an attacker may leverage this issue of XSS to execute arbitrary script code in the browser of an unsuspecting user in the context of the affected site. This may allow the attacker to steal cookie-based authentication credentials and to launch other attacks. Also, the vulnerability is related to the "get_the_generator" function because the version string is not properly escaped in the function. As mentioned, attackers can exploit this vulnerability easily to execute arbitrary malicious Web script or HTML code in the affected browser, resulting in XSS attacks.
    
    •	How it was fixed/patched
    Upgrading to version 4.9.5 eliminates this vulnerability. WordPress versions 4.9.4 and earlier were affected by three security issues which were eventually fixed and implemented in 4.9.5. The fixes were: Don't treat localhost as same host by default, use safe redirects when redirecting the login page if SSL is forced and make sure the version string is correctly escaped for use in generator tags. Overall, 25 other bugs were fixed in WordPress 4.9.5.

    Reference: 
    https://wordpress.org/news/2018/04/wordpress-4-9-5-security-and-maintenance-release/
    https://www.securityfocus.com/bid/103775/references
    https://vuldb.com/?id.116227

### 3) CVE-2018-6389

    In WordPress through 4.9.2, unauthenticated attackers can cause a denial of service (resource consumption) by using the large list of registered .js files (from wp-includes/script-loader.php) to construct a series of requests to load every file many times.	
    Publish Date : 2018-02-06, Last Update Date : 2018-03-05
