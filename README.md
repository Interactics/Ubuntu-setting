# Ubuntu setting

## Change Server from KAIST to KAKAO

    sudo sed -i 's/kr.archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list  #KOREA
    sudo sed -i 's/archive.ubuntu.com/mirror.kakao.com/g' /etc/apt/sources.list # 미국

## vim setting 
copy `vimrc.txt` and paste at `~/.vimrc`

## terminator setting 

### requirement 

    sudo apt install fonts-naver-d2coding


copy `terminator_setting.txt` and paste at `~/.config/terminator/config`
