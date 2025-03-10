name: Check URLs

on: [push, pull_request]

jobs:
  urls:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Set up Ruby
        uses: ruby/setup-ruby@v1
        with:
          ruby-version: 2.6

      - name: Install awesome_bot
        run: gem install awesome_bot

      - name: Check URLs
        run: awesome_bot README.md --allow-redirect --request-delay 0.2 -w gbstandards.org,iec.ch,gost.ru,tcvn.gov.vn,tisi.go.th# 888
移动到页面上的下一个交互元素。编辑README.md文件内容
#项目名称
##简介
这是我的第一个 GitHub 项目，用于实现 XXX 功能。

##如何使用
1. 下载文件：点击。
2. 解压后打开 `index.html`，即可运行。

