# readme
A cheatsheet for CTFs, that will eventually hopefully have everything that I know of.

General markdown for topics:
  1. Explanation
  2. Common vulns that I've learned
  3. Tools and how to use them

https://www.exploit-db.com/
  
# Crypto

bytes.fromhex(), base64.b64encode(), base64.b64decode(), Crypto.Util.number.long_to_bytes()
  
  <code>byte_xor.py</code> in scripts

# pwn
Python pwntools library
  
* use remote(HOST, PORT, level='debug')
  
# rev
_gdb_
_ghidra_
  
## Android APKs
  1) APK decompiler https://www.decompiler.com/ or use installed _jadx_ app
  2) Look into _/Resources/AndroidManifest.xml_ and then search _/sources_ for _MainActivity.java_ and work on from there. _R.java_ could also be of use.
  3) Android Studio can be useful for viewing files and actually running the APK  

  Reversing guide and exercises: https://www.ragingrock.com/AndroidAppRE/
  https://en.wikipedia.org/wiki/Apk_(file_format)

## wireshark
- https://github.com/welchbj/ctf/blob/master/docs/pcap.md
- file extraction: https://www.sneakymonkey.net/2017/03/03/pcap-file-extraction/
- WireShark webpage for common vulns

- MITM attacks
- ARP poisoning
  
## images

  - Varius 2D codes -> QR Code, MaxiCode, Aztec etc
  - https://www.photopea.com/
    -> online photoshop
  - https://stegonline.georgeom.net/upload
    -> bit plane browsing, extract data, show info and strings
  - Python Pillow (PIL) for working with pixel data
  
  **exiftool**<br>
    * look at image size
    * either use hex editor (remember little endian) or <code>convert in.jpg -resize INTxINT out.jpg</code>
    * can alter some things, comments for example
  
 **imagemagick and ffmpeg**
  <br><code> ffmpeg -i video.mp4 -vf mpdecimate,setpts=N/FRAME_RATE/TB frames/frame_%3d.jpg # get frames from video </code><br>
  <code> convert frames/frame_*.jpg -compose Darken -layers Flatten result.jpg # join multiple images of frames together </code>
 
 ** Bitwise operations (code in scripts)
  
  Tools:
  _strings_, _zsteg_, _xxd_, _binwalk_, _steghide_, _stegsolve_, _foremost_, _stat_, 
  
## audio
  - audacity
    * audio spectrogram -> "a spectrogram is a visual representation of the spectrum of frequencies of sound, or other signals, as they vary with time." Basically, it is a method to visualize sound and signals. Can pretty much hide anything from messages to images and so on.
  
  - dtmf-decoder _dtmf_ on linux or https://unframework.github.io/dtmf-detect/

  - a butt load of decoders
    * https://www.reddit.com/r/RTLSDR/comments/1e37d0/linux_software_to_decode_digital_modes/
  
## videos
  - ffmpeg and imagemagick
    -> https://gist.github.com/sulram/0c8a95fc90f23e860b9a
  
## malware
  - powerpoints and similar can be unzipped
  - _vbaProject.bin_ contains macros
  - ProcessHacker 2 can help with c&c or similar
  - VirusTotal can detect stuff
  
 _olevba_

  - Malware detection https://www.virustotal.com/gui/home/upload
# Misc
  
# Useful for CTFs
  
* https://github.com/JohnHammond/ctf-katana
