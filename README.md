# CSE 135 – HW1

Live Site: https://enjoypudology.com/

GitHub Repository: https://github.com/SyrineMekni/enjoypudology

Deploy Setup:

1. Website files are edited locally and committed to the GitHub repository.
2. Changes are pushed to GitHub using:
   - `git add .`
   - `git commit -m "message"`
   - `git push`
3. GitHub sends a webhook POST request to the server at:
   - `http://137.184.3.163:9000/hooks/deploy-enjoypudology`
4. The server runs a deploy script that pulls the latest version of the repository into:
   - `/var/www/enjoypudology.com`
5. Refreshing the live site shows the updated content.

The demo : `Github-Deploy.gif`
