rails-ubuntu-express-install 快速安裝
=============================

這個是以能建立開發環境為主

首先安裝一台 Ubuntu 機器 (建議10.x 版本以上 這裡用 12.04 作為示範)

安裝系統環境:
-------------

	sudo add-apt-repository ppa:chris-lea/node.js
	sudo apt-get update 
	sudo apt-get install git core install libxml2 libxml2-dev libxslt1-dev nodejs


安裝Ruby (使用rubyenv)
----------------------

在命令列打入

	curl https://raw.github.com/fesplugas/rbenv-installer/master/bin/rbenv-installer | bash	

將以下這些加到你的`.bashrc`裡 

	export RBENV_ROOT="${HOME}/.rbenv"

	if [ -d "${RBENV_ROOT}" ]; then
	  export PATH="${RBENV_ROOT}/bin:${PATH}"
	  eval "$(rbenv init -)"
	fi

完成後打`source ～.bashrc` 環境設定檔

輸入

	rbenv bootstrap-ubuntu-12-04

完成後開始安裝Ruby(最新版請參考官方網站的版本號 目前是1.9.3-p286)

輸入

	rbenv install 1.9.3-p286

安裝完畢後輸入

	rbenv global 1.9.3-p286

設定系統全域使用該個版本 可以使用 `ruby -v` 來檢查是否安裝正確

最後一步 安裝 Rails
-------------------

命令列輸入

	gem install rails 
	rbenv rehash

到這裡就安裝完成了！

接下來你就可以找個地方 `rails new [project name]` 開始體驗 Ruby on Rails 強大的功能:D
