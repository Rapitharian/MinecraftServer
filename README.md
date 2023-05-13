# MinecraftServer
-Location: /etc/systemd/system/minecraft.server
-cp minecraft.server /etc/systemd/system/
-systemctl daemon-reload
-semanage fcontext -a -t bin_t /home/minecraft/server
-semanage fcontext -a -t bin_t /home/minecraft/server/minecraft.jar
-restorecon -Rv /home/minecraft/server
-systemctl start minecraft.server
-journalctl -fu minecraft.server
