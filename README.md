## Elasticsearch-kibana_yml

錯誤解決：max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]




> 然後可以執行以下命令，設置 vm.max_map_count ，但是重啟後又恢復為預設值。

sudo sysctl -w vm.max_map_count=262144
```
sudo sysctl -p
```
or 永久改變
```
sudo vim /etc/sysctl.conf
vm.max_map_count=262144
sudo sysctl -p
```
