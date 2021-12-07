## JenkinsPC Setting メモ
- Mac をスリープさせないようにする
  - Automator.appの作成
  - nohup caffeinate -d


- インストール
  - Chrome
  - Google日本語入力
  - UnityHub
  - SourceTree
  - homebrew
  - Jenkins
    - brew install git
    - brew install Jenkins-lts
  - 設定
    - PC起動時にJenkinsが起動するように設定
    - cp -p /usr/local/opt/jenkins/*.plist
    - ~/Library/LaunchAgentslaunchctl load
    - ~/Library/LaunchAgents/homebrew.mxcl.jenkins.plist
  - 外部PCからの接続許可(下記を削除)
```
<string>--httpListenAddress=127.0.0.1</string>
<string>--httpPort=8080</string>
```
  - 再起動
  - リモート接続設定
  - 「共有」->リモートマネージメントON
  - Jenkins内部設定
    - 設定→グローバルプロパティ→環境変数→
      - KEYCHAIN_PW
        - パスワード入れる
      - LOGIN_KEYCHAIN_PATH
        - $HOME/Library/Keychains/login.keychain-db
      - NDK_PATH
        - $HOME/Library/Android/sdk/android-ndk-r16b
      - Path
        - /usr/local/bin:$PATH
      - SDK_PATH
        - $HOME/Library/Android/sdk
      - JDK_PATH
        - /Library/Java/JavaVirtualMachines/openjdk-11.jdk/Contents/Home
      - javaArgs
        - -Dfile.encoding=UTF-8 -Dsun.jnu.encoding=UTF-8 -Djava.io.tmpdir=/Users/~~~~/jenkins_home/tmp -Xmx2048m
    - 内部認証(git sshキー設定)
    - Pulgin
      - build user vars
      - https://plugins.jenkins.io/build-user-vars-plugin/
      - Parameterized Trigger
      - https://plugins.jenkins.io/parameterized-trigger/
      - 以前使用していたPluginがinstall出来ない場合は手動でinstall
      - ($JENKINS_HOME/plugins) に格納

- Xcode指定

` DEVELOPER_DIR=/Applications/Xcode12.4.app/Contents/Developer xcodebuild \`
