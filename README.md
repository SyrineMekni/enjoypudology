# CSE 135 – HW1

## Live Site
https://enjoypudology.com/

## GitHub Repository
https://github.com/SyrineMekni/enjoypudology

Team member: Syrine Mekni
Grader username: grader
Grader password: Rightpath@333


## GitHub Auto-Deploy Setup
This site is deployed automatically from GitHub to my DigitalOcean server using a webhook.

### How deploy works
1. Website files are edited and committed to the GitHub repository.
2. Changes are pushed using:
   - git add .
   - git commit -m "message"
   - git push
3. GitHub sends a webhook POST request to:
   - http://137.184.3.163:9000/hooks/deploy-enjoypudology
4. The server runs a deploy script that pulls the latest code into:
   - /var/www/enjoypudology.com
5. Refreshing the site shows the live updates.

### Deploy Demo
- 'Github-Deploy.gif'

---

## HW1 Part 3 – Server Configuration

### PHP and MySQL
- Installed MySQL and PHP
- Created PHP test page:
  - '/var/www/enjoypudology.com/hw1/hello.php'
- Screenshot: `php-verification.png`

### Basic Authentication
- Enabled password protection for the team site
- Created user: 'grader'
- Login credentials are provided in the Gradescope submission

### Compression
- Enabled gzip/deflate compression for HTML, CSS, and JavaScript
- Verified in Chrome DevTools:
  - 'Content-Encoding: gzip'
- Screenshot: 'compress-verify.png'

### Server Header
Attempted to modify Server header to "CSE135 Server".
Ubuntu Apache does not allow full override.


### Custom 404 Page
- Created '404.html'
- Configured Apache to route 404 errors to this page
- Screenshot: `error-page.png`

### Logs and Analytics
- Access logs located at:
  - '/var/log/apache2/enjoypudology_access.log'
- Generated GoAccess report:
  - '/var/www/enjoypudology.com/hw1/report.html'
- Screenshots:
  - 'log-verification.png'
  - 'report-verification.png'
