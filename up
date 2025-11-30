
# Setup 

* Windows

```
https://scoop.sh/
```

```
scoop bucket add extras
scoop install extras/mkvtoolnix

scoop bucket add main
scoop install main/ffmpeg
scoop install main/mediainfo
scoop install main/bento4

https://github.com/shaka-project/shaka-packager/releases/tag/v2.6.1
https://github.com/quietvoid/dovi_tool/releases
```

* MacOS 


```
https://formulae.brew.sh/
```

```
brew install ffmpeg
brew install mkvtoolnix
brew install mediainfo
brew install bento4

https://github.com/shaka-project/shaka-packager/releases/tag/v2.6.1
https://github.com/quietvoid/dovi_tool/releases
```


# How to use 

* Use Chrome Extension 



# Command 

```
Usage: vdr {download|-d} [OPTIONS] <COMMAND>

Commands:
  MGTV     Download Mango Plus content
  MGI      Download MangoTV content
  VIEON    Download VieON content
  YK       Download Youku content
  YKTV     Download Youku TV content
  WETV     Download WETV content
  IQ       Download IQ content
  NF       Download Netflix content
  FPT      Download FPTPlay content
  BILI     Download Bilibili content
  CR       Download Crunchyroll content
  GXPL     Download GalaxyPlay content
  KKTV     Download KKTV content
  MYTV     Download MyTV content
  TV360    Download TV360 content
  VIU      Download Viu content
  KCW      Download Kocowa content
  SCTV     Download SCTV content
  THVL     Download THVL content
  LINE     Download LineTV content
  MYVIDEO  Download MyVideo content
  TVBAW    Download TVBAnywhere content
  KPLUS    Download Kplus content
  help     Print this message or the help of the given subcommand(s)

Options:
  -q, --quality <QUALITY>          Specify download resolutions
  -c, --credentials <CREDENTIALS>  Credentials for authentication
  -v, --v-codec <VIDEO_CODEC>      Preferred video codec [possible values: avc, hevc, vc1, vp8, vp9, av1]
  -f, --fps <FPS>                  Preferred frames per second
  -r, --range <RANGE>              Video range (e.g., HDR, SDR) [possible values: sdr, hdr, dolby-vision, hybrid]
  -a, --a-codec <AUDIO_CODEC>      Preferred audio codec [possible values: aac, ac3, ac4, he-aac, eac3]
  -w, --wanted <WANTED>            Select episodes to download
      --m-lang <MAIN_LANG>         Set main language
      --a-lang <LANG>              Preferred audio language(s)
      --s-lang <S_LANG>            Preferred subtitle language(s)
  -V, --video-only                 Download only the video
  -A, --audio-only                 Download only the audio
  -S, --subs-only                  Download only subtitles
      --slow <SLOW>                Introduce delays during download
      --skip-dl                    Skip downloading actual media content
      --skip-merge                 Skip merging downloaded media content
  -t, --text                       Text search mode
  -n, --name <NAME>                Set name
  -k, --key <KEYS>                 Set key for DRM
      --sub <SUB_PATH>             Add subtitles to manifest
      --append                     Append subtitles mode to manifest (true = append, false = overwrite)
  -h, --help                       Print help

```



# Arg --m-lang

* Dùng để đặt ngôn ngữ gốc của Audio (ví dụ trong MPD của TV360 luôn là eng muốn đổi sang vi) (chọn ở extension) 
* Track chỉ có 1 audio hoặc audio là "und" sẽ được đặt thành main lang 

```
vdr --m-lang="vi"
```

# Arg -n | --name 

* Dùng để đặt tên khi tên phim là tiếng trung 

```
vdr ... -n="Doraemon"
```

* Nếu thêm "|{index}" sẽ đặt season Index = index nếu chỉ có 1 season (không tính season 0 thì đây là trailer hoặc bonus).

```
vdr ... -n="Doraemon|3" => title: Doraemon, season_idx: 3
```

# Arg --sub 
* Dùng để mux thêm sub rời (cho Youku, Tencent nội địa) 
* Nếu thêm từ --append sẽ không xoá phụ đề gốc 

```
vdr ... --sub="{folder_location} YK ... (không append vì sub gốc lệch)
```

# MYTV 

* Lấy danh sách chiếu trong ngày hiện tại

```
vdr ... MYTV "https://mytv.com.vn/truyen-hinh/210"
```

* Chỉ lấy link live (DRM NOT WORK)

```
vdr ... MYTV "https://mytv.com.vn/truyen-hinh/210" --live
```

* Lấy vod cụ thể (khi chọn vào chương trình ở lịch phát sóng trên trình duyệt)
```
vdr ... MYTV "https://mytv.com.vn/truyen-hinh/210?date=251129&st=0850&et=0900"
```

* Lấy lịch chiếu theo ngày
```
vdr ... MYTV "https://mytv.com.vn/truyen-hinh/210?date=251129"
```

# IQ 

* Tải theo vùng 

```
vdr ... IQ "link" -c {region}
```

* Tìm theo trên

```
vdr ... -t IQ "abc"
```

# Netflix 

* Một số phim không có DDP cần thêm -a để lấy HE-AAC 

```
vdr ... NF {id} -a
```

