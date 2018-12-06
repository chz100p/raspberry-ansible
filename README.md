# raspberry-ansible

Ansibleでゼロワンシリーズを使うRaspberry Piに環境を構築するサンプルPlaybookです。

## Requirements
- ansible 2.2 or later

## Usage

### Raspberry Pi

以下URLのRaspbianをインストールしたRaspberry Piを準備し、
SSH接続可能な環境を構築しておいてください。

- Raspbian STRETCH WITH DESKTOP(Release date:2017-09-07)
https://www.raspberrypi.org/downloads/raspbian/


### Download
適当なディレクトリにPlaybookをダウンロードしてください。

```
$ git clone https://github.com/chz100p/raspberry-ansible.git
$ cd raspberry-ansible
$ git checkout zero_one
```

### Edit hosts

hosts.sampleファイルがあるので、hostsにコピーしてください。
```
$ cp hosts.sample hosts
```

hostsにRaspberry PiのIPアドレスを記載してください。

```
[raspberry-pi]
XX.XX.XX.XX # set your environment
```

### Execute ansible

ansibleを実行してください。
対象としたRaspberry Piに環境が構築できます。

```
$ ansible-playbook site.yml -v
```
