# Configuración iptables para systemd

Ejemplo de configuración de cortafuegos iptables para systemd en Ubuntu.
Probado en Ubuntu 15.10 - Enero 2016

### Pasos para la instalación
Realizar con permisos de administrador (root)
```sh
cp -r etc  /
cp -r lib  /

systemctl daemon-reload
systemctl enable iptables.service
systemctl start  iptables.service
```

Referencias:
Basado en el trabajo https://github.com/gronke/systemd-iptables 
