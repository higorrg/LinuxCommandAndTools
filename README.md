# Linux Command and Tools

## SystemD vs SystemV

<table>
  <tr>
   <td><strong>Description</strong>
   </td>
   <td><strong><code>SystemD</code></strong>
   </td>
   <td><strong><code>SystemV</code></strong>
   </td>
  </tr>
  <tr>
   <td>Start a service
   </td>
   <td><code>systemctl <strong>start</strong> {x}</code>
   </td>
   <td><code>service {x} start</code>
   </td>
  </tr>
  <tr>
   <td>Stop a service
   </td>
   <td><code>systemctl <strong>stop</strong> {x}</code>
   </td>
   <td><code>service {x} stop</code>
   </td>
  </tr>
  <tr>
   <td>Restart a service
   </td>
   <td><code>systemctl <strong>restart</strong> {x}</code>
   </td>
   <td><code>service {x} restart</code>
   </td>
  </tr>
  <tr>
   <td>Check if a service is running
   </td>
   <td><code>systemctl <strong>is-active</strong> {x}</code>
   </td>
   <td><code>service {x} status</code>
   </td>
  </tr>
  <tr>
   <td>Install service
   </td>
   <td><code>systemctl <strong>enable</strong> {x}</code>
   </td>
   <td><code>chkconfig {x} on</code>
   </td>
  </tr>
  <tr>
   <td>Uninstall a service
   </td>
   <td><code>systemctl <strong>disable</strong> {x}</code>
   </td>
   <td><code>chkconfig {x} off</code>
   </td>
  </tr>
  <tr>
   <td>Check if a service is installed
   </td>
   <td><code>systemctl <strong>is-enabled</strong> {x}</code>
   </td>
   <td><code>chkconfig {x} --list</code>
   </td>
  </tr>
  <tr>
   <td>Turn off the computer/vm/system
   </td>
   <td><code>systemctl <strong>halt/poweroff</strong></code>
   </td>
   <td><code>halt</code>
   </td>
  </tr>
  <tr>
   <td>Restart the computer/vm/system
   </td>
   <td><code>systemctl <strong>reboot</strong></code>
   </td>
   <td><code>reboot</code>
   </td>
  </tr>
  <tr>
   <td>Kill a process
   </td>
   <td><code>systemctl <strong>kill</strong> {x}</code>
   </td>
   <td><code>kill -9 {pid}</code>
   </td>
  </tr>
  <tr>
   <td>Show a unit’s dependencies
   </td>
   <td><code>systemctl list-dependencies</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>List sockets and what activates
   </td>
   <td><code>systemctl list-sockets</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>View active systemd jobs
   </td>
   <td><code>systemctl list-jobs</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>See unit files and their states
   </td>
   <td><code>systemctl list-unit-files</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Show if units are loaded/active
   </td>
   <td><code>systemctl list-units</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>List default target (like run level)
   </td>
   <td><code>systemctl get-default</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Set default target to start in graphical target (like run level 5)
   </td>
   <td><code>systemctl set-default graphical.target</code>
   </td>
    <td><code>init 5</code>
   </td>
  </tr>
  <tr>
   <td>Set default target to not start in graphical target (like run level 3)
   </td>
   <td><code>systemctl set-default multi-user.target</code>
   </td>
    <td><code>init 3</code>
   </td>
  </tr>
  <tr>
   <td>Follow messages as they appear
   </td>
   <td><strong><code>journalctl -f</code></strong>
   </td>
   <td><code>tail -f /var/log/messages</code>
   </td>
  </tr>
  <tr>
   <td>Show only kernel messages
   </td>
   <td><code>journalctl -k</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Show all error of this boot
   </td>
   <td><code>journalctl -b -p err</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Filter the log
   </td>
   <td><code>journalctl --since=today</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>See network service messages
   </td>
   <td><code>journalctl -u network.service</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Show all messages of a process
   </td>
   <td><code>journalctl /usr/sbin/httpd</code>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Print computer/vm/system informations
   </td>
   <td><strong><code>hostnamectl</code></strong>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Print date and time
   </td>
   <td><strong><code>timedatectl</code></strong>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Analyze boot time
   </td>
   <td><strong><code>systemd-analyze</code></strong>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Analyze boot critical path to graphic</td>
   <td><strong><code>systemd-analyze critical-chain graphical.target</code></strong></td>
   <td></td>
  </tr>
  <tr>
   <td>Analyze and debug system manager</td>
   <td><strong><code>systemd-analyze blame</code></strong></td>
   <td></td>
  </tr>
</table>
