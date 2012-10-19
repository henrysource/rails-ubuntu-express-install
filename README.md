rails-ubuntu-express-install 快速安裝
=============================

this is for rails developement enviroment 

first install your ubuntu (recommand 10.x or above) 
I will use 12.04 to demostrate

1. system enviroment

	sudo add-apt-repository ppa:chris-lea/node.js
	sudo apt-get update 
	sudo apt-get install git core 
	sudo apt-get install libxml2 libxml2-dev libxslt1-dev nodejs

2.install ruby by using rbenv

type

	curl https://raw.github.com/fesplugas/rbenv-installer/master/bin/rbenv-installer | bash	

add this in my youre .bashrc file 

	export RBENV_ROOT="${HOME}/.rbenv"

	if [ -d "${RBENV_ROOT}" ]; then
	  export PATH="${RBENV_ROOT}/bin:${PATH}"
	  eval "$(rbenv init -)"
	fi

type

	rbenv bootstrap-ubuntu-12-04

to install latest version of ruby please check official site

	rbenv install 1.9.3-p286
	rbenv global 1.9.3-p286

finally type 

	gem install rails 
	rbenv rehash

there you go. enjoy the power of rails :D

