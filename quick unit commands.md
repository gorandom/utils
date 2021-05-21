unix top largest big file:
du -a / | sort -n -r | head -n 10

unix process limit
sudo cat /proc/<PID>/limits

unix process resource usage
sudo ls -l /proc/<PID>/fd/ | wc -l

unix check open incomming connections to port 8000
sudo lsof -i TCP:8000 | wc -l

installing redis-cli in linux
wget https://download.redis.io/releases/redis-5.0.9.tar.gz
tar xzf redis-5.0.9.tar.gz
cd redis-5.0.9
make
echo "PATH=$PATH:$PWD/src" >> ~/.bash_profile
source ~/.bash_profile

Loading rdb file
./redis-5.0.7/src/redis-server --dbfilename dump.rdb --dir /path/to/file/location

