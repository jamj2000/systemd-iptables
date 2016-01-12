# Configuración iptables para systemd

**Ejemplo de configuración de cortafuegos iptables para systemd en Ubuntu.**

Probado en Ubuntu 15.10 ( Enero 2016 )

### Pasos para la instalación
Realizar estos pasos con permisos de administrador (root)
```sh
cp -r etc  /
cp -r lib  /

systemctl daemon-reload
systemctl enable iptables.service
systemctl start  iptables.service
```

**IMPORTANTE**: 

Por defecto el enrutamiento interno no viene activado. Para activar el enrutamiento interno de forma manual ejecuta
```sh
echo 1 > /proc/sys/net/ipv4/ip_forward
```
Si deseas que los cambios sean permanentes edita el archivo ```/etc/sysctl.conf``` y descomenta la línea
```
net.ipv4.ip_forward=1
```


### Referencias
Basado en:  https://github.com/gronke/systemd-iptables 
