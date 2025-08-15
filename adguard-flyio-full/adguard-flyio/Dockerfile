FROM adguard/adguardhome:latest

# Copy custom lists
COPY lists/denylist.txt /opt/adguardhome/conf/denylist.txt
COPY lists/allowlist.txt /opt/adguardhome/conf/allowlist.txt

# Set permissions
RUN chmod 644 /opt/adguardhome/conf/denylist.txt /opt/adguardhome/conf/allowlist.txt

# Start AdGuard Home
CMD ["/opt/adguardhome/AdGuardHome", "-c", "/opt/adguardhome/conf/AdGuardHome.yaml", "-w", "/opt/adguardhome/work"]
