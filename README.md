# Cloud-Computing-Assignment3
Creating a Microsoft Entra ID for Frontend Devs in my Organization

## STEPS
1. I created a group called "frontend-devs".
2. After wards I created microsoft entra IDs for 3 users.
3. Provisioned a VM resource from the main account.
4. From the Azure console, I created a role assignment granting Virtual machine contributor to users that belong to group "frontend-devs".

<img width="1280" height="800" alt="Screenshot 2026-04-13 at 12 30 59" src="https://github.com/user-attachments/assets/730b1e0c-ce93-4525-b338-b48dde0a8b03" />


5. I SSHed into the VM, then ran the following command prompts in the terminal:
```
sudo adduser newuser
sudo mkdir /home/newuser/.ssh
sudo nano /home/newuser/.ssh/authorized_keys
Inside the authorized_keys file, I pasted the public_keys of the users i created.
```

Then finally, I ran the following command.

```
sudo chown -R newuser:newuser /home/newuser/.ssh
sudo chmod 700 /home/newuser/.ssh
sudo chmod 600 /home/newuser/.ssh/authorized_keys
```
