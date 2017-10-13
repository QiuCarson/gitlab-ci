## 安装gitlab-runner

官网：https://gitlab.com/gitlab-org/gitlab-runner<br />
###### centos

`curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.rpm.sh | sudo bash`
`sudo yum install gitlab-runner`<br />

## 安装composer

`php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"`
php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"`
php composer-setup.php`
php -r "unlink('composer-setup.php');"`<br />

## 放到全局了，这样gitlab-ci执行的时候快

`composer global require phplint/phplint`
`composer global require squizlabs/php_codesniffer`
`composer global require 'sebastian/phpdcd=*'`
`composer global require "pdepend/pdepend:@stable"`
`composer global require phploc/phploc`
`composer global require "phpmd/phpmd:@stable"`<br />