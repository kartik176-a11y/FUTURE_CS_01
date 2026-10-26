# FUTURE_CS_01 — Website Vulnerability Assessment

## Project Overview
This project involved a basic website vulnerability assessment of **OWASP Juice Shop**, an intentionally vulnerable web application used for cybersecurity education and authorized security testing.

The application was run locally using Docker, and basic reconnaissance and security-header observations were performed using Nmap, cURL, browser Developer Tools, and OWASP ZAP.

## Objectives
- Identify accessible services and inspect the local web application.
- Review HTTP response headers.
- Observe potential security misconfigurations using OWASP ZAP.
- Document findings and include supporting evidence.
- Recommend security improvements.

## Tools Used
- **Docker Desktop** — Run OWASP Juice Shop locally.
- **Nmap** — Scan the local application port and inspect service information.
- **cURL** — Retrieve HTTP response headers.
- **Browser Developer Tools** — Inspect network activity and response headers.
- **OWASP ZAP** — Identify potential web security issues through passive scanning.

## Assessment Scope
- **Target:** OWASP Juice Shop running locally
- **URL:** `http://localhost:3000`
- **Port:** TCP 3000
- **Testing type:** Basic reconnaissance, HTTP-header review, and passive security scanning
- **Authorization:** Local educational lab environment

## Key Observations
1. The web application was accessible on TCP port 3000.
2. The HTTP response returned status `200 OK`.
3. The observed homepage response included headers such as `X-Content-Type-Options: nosniff` and `X-Frame-Options: SAMEORIGIN`.
4. OWASP ZAP reported potential security issues and informational alerts that require individual validation.
5. Findings may differ between application endpoints and responses; an alert does not automatically confirm an exploitable vulnerability.

## Evidence Included
- Nmap scan output
- HTTP response-header capture
- Browser Developer Tools screenshots
- OWASP ZAP alert screenshots
- Website Vulnerability Assessment Report (PDF)

## Recommendations
- Review and configure Content Security Policy (CSP).
- Validate security headers across relevant endpoints and responses.
- Review cross-origin resource-sharing (CORS) configuration.
- Minimize unnecessary information disclosure.
- Investigate and validate each scanner alert before classifying it as a confirmed vulnerability.
- Retest after applying security improvements.

## Limitations
This was a basic assessment of a local educational application. No production website was tested, and the scanner alerts were not all independently verified. The results should not be interpreted as a comprehensive penetration test.

## Disclaimer
This project was conducted for educational and cybersecurity training purposes against a locally hosted, intentionally vulnerable application. Test only systems for which you have explicit authorization.

## Author
**V. Karthik**  
Cybersecurity Student
