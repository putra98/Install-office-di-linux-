## Memperbarui Repository

Menginstall office di linux (Ubunutu 20.04) dengan menggunakn wine.

pertama-taman kita atu architecture 

```
apt-get dpkg --add-architecture i386
sudo dpkg --add-architecture i386
```

kita install wine

```
sudo apt-get install wine
```
kita atur prefix konfigurasi

```
WINEPREFIX=~/.wine/office2010 WINEARCH=win32 winecfg
```
kita install winbind cabextrac

```
sudo apt-get install winbind cabextrac
```

kita install winetricks bisa kalian kunjungin https://wiki.winehq.org/Winetricks#Installing_winetricks.

```
cd "${HOME}/Downloads"
wget  https://raw.githubusercontent.com/Winetricks/winetricks/master/src/winetricks
chmod +x winetricks
sudo cp winetricks /usr/local/bin
```
kita konfigurasi winetricks.
pilih 
- select the default
- install windows dll
- msxml6
- ok
- close

```
WINEPREFIX=~/.wine/office2010 WINEARCH=win32 winetricks
```

Kita check msxml6 apakah sudah terinstall

```
WINEPREFIX=~/.wine/office2010 WINEARCH=win32 winetricks msxml6
```

kita jalankan aplikasi

```
WINEPREFIX=~/.wine/office2010 WINEARCH=win32 wine ./setup.exe
```
