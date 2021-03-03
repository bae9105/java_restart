# java_restart
java_restart

java -varsion
openjdk version "11.0.9.1"

sudo vi ~/.bash_profile
export JAVA_HOME=$(/usr/libexec/java_home -v 11)
source ~/.bash_profile

환경변수 초기화 문제 
원인 : 터미널 테마 변경으로 zsh 쉘 때문 -> zsh는 터미널이 실행 될 때 ~/.zshrc가 실행
해결 : adb를 사용하기 위해 platform-tools가 지정되야함
      open . ~/.zshrc
      마지막 줄에 추가
      if [ -f ~/.bash_profile ]; then
	      . ~/.bash_profile
      fi
      
