|  コマンド  |  説明  |
| ---- | ---- |
| kubectl get services | 現在の名前空間上にあるすべてのサービスのリストを表示します|
| kubectl get pods --all-namespaces | すべての名前空間上にあるすべてのPodのリストを表示します|
| kubectl get pods -o wide | 現在の名前空間上にあるすべてのPodについてより詳細なリストを表示します|
| kubectl get deployment my-dep | 特定のDeploymentを表示します|
| kubectl get pods | 現在の名前空間上にあるすべてのPodのリストを表示します|
| kubectl get pod my-pod -o yaml| PodのYAMLを表示します
| kubectl get services --sort-by=.metadata.name | 名前順にソートしたServiceのリストを表示します |
| stern <Pod名> | アクセスログ確認表示 |
| nc -vz IP address | 接続疎通確認 |
| stern app | アクセスログ |
| kubectl get ing | ingress確認 |
| kustomize build | kubectl delete -f - | Resources削除 |
| kustomize build | kubectl apply -f - | Resources作成 |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
