---
# ROS依存関係ファイルの例
#
# このファイル (`example-rosdep.yaml`) は、ROSパッケージに必要なカスタム依存関係を定義するために使用されます。
# 特定のUbuntuディストリビューション（この場合はFocal）のための依存関係が記述されています。

# 使い方:
# この.yamlファイルを使用してROSの依存関係を管理するには、以下の手順に従ってください：

# 1. rosdep設定に追加:
#    - このファイルをローカルのrosdep設定に追加して、依存関係を解決できます。
#    - 以下のコマンドを実行して、rosdepのソースリストにこのファイルを追加します：
#      sudo sh -c 'echo "yaml file://path/to/example-rosdep.yaml" > /etc/ros/rosdep/sources.list.d/50-custom-dependency.list'
#      rosdep update

# 2. パッケージのインストール:
#    - `rosdep install` コマンドを使用して、ROSパッケージの依存関係を解決し、必要なパッケージをインストールします。

# ファイルの内容:
my_custom_package:
  ubuntu:
    focal:
      apt:
        packages:
          - libexample-dev
          - libexample-tools
