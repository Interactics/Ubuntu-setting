# Ubuntu setting

## time sync

    timedatectl set-local-rtc 1 -- adjust-system-clock

## Change Server from KAIST to KAKAO

    sudo sed -i 's/kr.archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list  #KOREA
    sudo sed -i 's/archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list # 미국
    sudo sed -i 's/ports.ubuntu.com/ftp.harukasan.org/g' /etc/apt/sources.list # 라즈베리 파이
    

## vim setting 
copy `vimrc.txt` and paste at `~/.vimrc`

## 우분투 한글 설정
1. Terminal에서 uim을 설치한다.

```
sudo apt-get install uim
```    

2. `setting` → `Region & Language` 항목의 `Manage installed Language` 클릭 입력기를 UIM으로 변경
    
3. Input Method 프로그램 실행하기

- `Global Settings`에서 `Specify default IM` 체크
- `Global Settings > Default Input method`를 `Byeoru`로 선택
- `Toolbar`의 `Display`를 `Never`로 설정
- `Global key bindings 1`의 상단의 `[Global] on`과 `[Global] off` 항목을 빈 칸으로 설정
- `setting` → `keyboard` → `windows` → `Activate the window menu` → `Disabled` (Backspace)
- `Byeoru key bindings 1`의 `[Byeoru] on`과 `[Byeoru] off` 키 설정을 `Multi_key`로 설정
이때 `Multi_key`는 한/영 변환키로 쓸 명령어를 사용하자. 
`alt + space`

4.  `setting` → `Region & Language`에서 `Korean(Hangul)` 추가 후 재부팅 하기.
    


## terminator setting 

## tmux setting 

### requirement 

    sudo apt install fonts-naver-d2coding


copy `terminator_setting.txt` and paste at `~/.config/terminator/config`

## Memory Swap 
    sudo swapoff -v /swapfile # 비활성화
    sudo fallocate -l 8G /swapfile # 8G 설정
    sudo chmod 600 /swapfile
    sudo mkswap /swapfile
    sudo swapon /swapfile
    
    # /etc/fstab 에서
    swapfile none swap sw 0 0
    
    # 확인 
    free -m 
