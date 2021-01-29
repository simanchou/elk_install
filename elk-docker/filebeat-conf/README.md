#filebeat install

sudo rpm --import https://packages.elastic.co/GPG-KEY-elasticsearch

cat <<EOF >/etc/yum.repos.d/elastic.repo
[elastic-7.x]
name=Elastic repository for 7.x packages
baseurl=https://artifacts.elastic.co/packages/7.x/yum
gpgcheck=1
gpgkey=https://artifacts.elastic.co/GPG-KEY-elasticsearch
enabled=1
autorefresh=1
type=rpm-md
EOF

sudo yum makecache
sudo yum install -y filebeat
#sudo systemctl enable filebeat
