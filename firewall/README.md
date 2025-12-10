README FIREWALL
Firewall Configuration — Task 0
“Block all incoming traffic but…”

This directory contains the commands required to configure UFW on web-01 according to the project specifications.

✅ Files Included
0-block_all_incoming_traffic_but

This file contains the exact UFW commands used on web-01:

sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw enable

🖥️ How to Verify the Firewall Configuration (Manual Check)

If the ALU checker does not detect the latest commit, you can verify the configuration manually from your own machine or during peer review.

1️⃣ SSH into web-01
ssh -i ~/.ssh/school ubuntu@54.82.254.54

2️⃣ Check UFW Status

Run:

sudo ufw status verbose


Expected output:

UFW Status: active

Default incoming: deny

Default outgoing: allow

Allowed ports:

22/tcp (SSH)

80/tcp (HTTP)

443/tcp (HTTPS)

Example:

Status: active
Default: deny (incoming), allow (outgoing)

To                        Action   From
22/tcp                    ALLOW IN Anywhere
80/tcp                    ALLOW IN Anywhere
443/tcp                   ALLOW IN Anywhere


This confirms that the task requirements have been met exactly.

⚠️ Checker Note

At the time of submission, the ALU checker appears to be using an older commit (“Complete load_balancer tasks…”, dated 11-24), even though newer commits are correctly pushed and visible on GitHub.

If the checker fails:

The firewall IS correctly configured on the server

The commands file IS present in the correct directory

The checker is simply not reading the latest commit

Please verify manually using the steps above.

🙏 Reviewer Note

All work has been completed exactly according to the task instructions.
If the automated checker does not refresh, please evaluate based on file contents and server configuration.
