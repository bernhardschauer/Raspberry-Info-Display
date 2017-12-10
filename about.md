# 1. Schritt - Vorbreitung der SD Karte (Noobs Dateien kopieren)

Unter https://www.raspberrypi.org/downloads/noobs/ kann die aktuelle Version von Noobs heruntergeladen werden. Die Datei wird dann auf die MicroSD Karte entpackt (wichtig: die Dateien müssen direkt im Hauptverzeichniss liegen, nicht in einem Unterordner)

Die MicroSD Karte muss FAT32 formartiert sein, meine neue 16 GB SanDisk war das ab Werk.

Bei der Lite Version ist das spätere Betriebssystem Raspbian noch nicht enthalten, dieses wird dann im zweiten Schritt via Internet nachgeladen.

# 2. Schritt - SD Karte in Raspberry Pi
Der Raspberry ist mit Monitor, Maus, Tastatur und Strom verbunden. Die vorbereitete Mirco SD Karte ist eingelegt. Nun startert der Raspberry automatisch.


# 3. Schritt - Erster Start
Nach der Installation startet das Betriebssystem erstmals und schlussendlich wird der Desktop angezeigt.
An meinem Monitor sind außen um das Bild schwarze Ränder (Oversampling). Unter Einstellungen - Raspberry-Pi-Konfiguration können diese ausgeblendet werden (Übertastung deaktivieren)

# 4. Schritt - Aktualisieren

'sudo apt-get update
sudo apt-get upgrade
sudo apt-get install unclutter

sudo nano /home/pi/.config/lxsession/LXDE-pi/autostart

#@xscreensaver -no-splash  # comment this line out to disable screensaver
@xset s off
@xset -dpms
@xset s noblank
@chromium-browser -noerrdialogs --kiosk http://solartv.solarweb.com
'
