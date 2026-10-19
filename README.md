## Setup Lightvela VPS Free 1Month

1. Login & klik free trial https://lightvela.ai/?ref=JVPTMWYZDG
2. Create Agent & Setup Tailscale ssh
3. Connect Tailscale ssh user root

# Uninstall Agent Hermes
```
hermes stop
systemctl --user stop hermes 2>/dev/null
sudo systemctl stop hermes 2>/dev/null
```
```
systemctl --user disable hermes 2>/dev/null
sudo systemctl disable hermes 2>/dev/null

rm -f ~/.config/systemd/user/hermes.service
sudo rm -f /etc/systemd/system/hermes.service

systemctl --user daemon-reload
sudo systemctl daemon-reload
```
```
uv tool uninstall hermes-agent 2>/dev/null
pip uninstall -y hermes-agent 2>/dev/null
pip3 uninstall -y hermes-agent 2>/dev/null
```
```
rm -rf ~/.hermes
rm -rf ~/.config/hermes
rm -rf ~/.cache/hermes
rm -rf ~/.local/share/hermes
rm -rf ~/hermes-agent
rm -rf ~/hermes
```
```
pkill -f '[h]ermes-agent'
pkill -f '[h]ermes'
```
```
command -v hermes
pip show hermes-agent
uv tool list
systemctl --user list-unit-files | grep -i hermes
sudo systemctl list-unit-files | grep -i hermes
```
``
cd /home/
``
```
rm -rf agentuser
rm -rf ubuntu
rm -rf lightclaw
```
# Delete user agentuser,ubuntu,lightclaw
```
userdel -r ubuntu
userdel -r lightclaw
userdel -r agentuser
```
```
userdel -r agentuser
```
```
kill id process
```
```
for u in ubuntu lightclaw agentuser; do
    if id "$u" >/dev/null 2>&1; then
        echo "$u masih ada"
    else
        echo "$u sudah terhapus"
    fi
done
```
# Add Password & Edit Permit Root Login
```
passwd root
```
```
nano /etc/ssh/sshd_config
```
- PermitRootLogin yes
- PasswordAuthentication yes
- ctrl + x + y
- reboot

# Disable Tailscale SSH
```
tailscale set --ssh=false
```



