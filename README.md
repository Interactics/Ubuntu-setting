# Ubuntu setting

## Change Server from KAIST to KAKAO

    sudo sed -i 's/kr.archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list  #KOREA
    sudo sed -i 's/archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list # 미국
    sudo sed -i 's/ports.ubuntu.com/ftp.harukasan.org/g' /etc/apt/sources.list # 라즈베리 파이

## vim setting 
copy `vimrc.txt` and paste at `~/.vimrc`

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
