- iOS ビルド時にPodの作成がうまく行われないのはpadのinstall漏れ
    - [podがうまくインストールされない](https://qiita.com/spring_i/items/181bc3c05142d1f80d93)
    - Gemとの依存関係でうまく入らないので、一度Podを削除してrbenvでRubyを指定しなおす
    - [gem installでpermissionエラーになった時の対応方法](https://qiita.com/nishina555/items/63ebd4a508a09c481150)
    - [CocoaPodsのインストールで手間取ったこと](https://qiita.com/spring_i/items/181bc3c05142d1f80d93)

|  コマンド  |  詳細  |
| ---- | ---- |
| sudo gem install cocoapods | インストール |
| sudo gem install cocoapods-deintegrate | CocoaPodsを完全削除 |
| pod --version | Pod確認 |
|  |  |
|  |  |
|  |  |


