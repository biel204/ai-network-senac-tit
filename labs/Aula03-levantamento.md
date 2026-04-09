  UNIT                        LOAD   ACTIVE SUB     DESCRIPTION                                   
  apache2.service             loaded active running The Apache HTTP Server
  cron.service                loaded active running Regular background program processing daemon
  dbus.service                loaded active running D-Bus System Message Bus
  fwupd.service               loaded active running Firmware update daemon
  getty@tty1.service          loaded active running Getty on tty1
  grafana-server.service      loaded active running Grafana instance
  ModemManager.service        loaded active running Modem Manager
  multipathd.service          loaded active running Device-Mapper Multipath Device Controller
  mysql.service               loaded active running MySQL Community Server
  node_exporter.service       loaded active running Node Exporter
  polkit.service              loaded active running Authorization Manager
  prometheus.service          loaded active running Prometheus
  rsyslog.service             loaded active running System Logging Service
  ssh.service                 loaded active running OpenBSD Secure Shell server
  systemd-journald.service    loaded active running Journal Service
  systemd-logind.service      loaded active running User Login Management
  systemd-networkd.service    loaded active running Network Configuration
  systemd-resolved.service    loaded active running Network Name ResolutionS
  systemd-timesyncd.service   loaded active running Network Time Synchronization
  systemd-udevd.service       loaded active running Rule-based Manager for Device Events and Files
  tomcat11.service            loaded active running Apache Tomcat11

  Netid                    State                     Recv-Q                    Send-Q                                       Local Address:Port                                         Peer Address:Port                    Process
udp                      UNCONN                    0                         0                                               127.0.0.54:53                                                0.0.0.0:*
udp                      UNCONN                    0                         0                                            127.0.0.53%lo:53                                                0.0.0.0:*
tcp                      LISTEN                    0                         4096                                         127.0.0.53%lo:53                                                0.0.0.0:*
tcp                      LISTEN                    0                         300                                                0.0.0.0:3306                                              0.0.0.0:*
tcp                      LISTEN                    0                         4096                                            127.0.0.54:53                                                0.0.0.0:*
tcp                      LISTEN                    0                         4096                                               0.0.0.0:22                                                0.0.0.0:*
tcp                      LISTEN                    0                         4096                                                     *:3000                                                    *:*
tcp                      LISTEN                    0                         4096                                                     *:9091                                                    *:*
tcp                      LISTEN                    0                         4096                                                     *:9100                                                    *:*
tcp                      LISTEN                    0                         100                                                      *:8080                                                    *:*
tcp                      LISTEN                    0                         511                                                      *:8888                                                    *:*
tcp                      LISTEN                    0                         70                                                       *:33060                                                   *:*
tcp                      LISTEN                    0                         511                                                      *:80                                                      *:*
