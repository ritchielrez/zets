## Dpkg proccess lock fix

Run to fix the dpkg proccess lock problem, solve provided by a primary
dpkg developer. 
```bash
sudo fuser -vik -TERM /var/lib/dpkg/lock /var/lib/dpkg/lock-frontend /var/lib/apt/lists/lock
sudo dpkg --configure --pending
```
