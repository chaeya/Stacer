# HamoniKR Stacer

[Stacer] (https://github.com/oguzhaninan/Stacer/) 프로젝트를 하모니카 3.0 에서 사용할 수 있도록 수정해서 배포한 프로그램

## 수정사항

 * 한글 사용자를 위한 폰트 및 UI 변경
 * 한글 언어 추가
 * 하모니카OS 에서 테스트 완료된 기능만 포함
 * 빌드 환경 QT 5.9 지원하게 변경 (하모니카 3.0 기본 설치 환경)

## Screenshots

<p align="center">
    <img src="screenshots/stacer.png" width="700">
</p>

# Install 

### 프로그램에 필요한 필수 패키지
- curl, systemd

### HamoniKR 3.0
```
sudo apt-get install stacer -y
```


### ubuntu 18.04
```
wget -O - http://apt.hamonikr.org/hamonikr.key| sudo apt-key add -
sudo bash -c "echo 'deb https://apt.hamonikr.org sun main upstream' > /etc/apt/sources.list.d/hamonikr.list"
sudo apt update
sudo apt-get install stacer -y
```

### Debian x64

1. Download `stacer_1.1.0_amd64.deb` from the [releases page](https://github.com/chaeya/Stacer/releases/tag/1.1.0hamonikr1).
2. Run `sudo dpkg -i stacer*.deb` on the downloaded package.
3. Launch Stacer using the installed `stacer` command.


### Build from source with CMake (HamoniKR 3.0)

1. sudo apt insall qt5-default -y
2. mkdir build && cd build
3. cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_PREFIX_PATH=/usr/lib/x86_64-linux-gnu/qt5/bin ..
4. make -j $(nproc)
5. output/bin/stacer

