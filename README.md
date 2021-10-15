## Elasticsearch-kibana_yml

錯誤解決：max virtual memory areas vm.max_map_count [65530] is too low, increase to at least [262144]


> 先要切換到root；

> 然後可以執行以下命令，設置 vm.max_map_count ，但是重啟後又会恢復為預設值。

```python
sysctl -w vm.max_map_count=262144
```
> 持久性的做法是在 /etc/sysctl.conf 文件中修改 vm.max_map_count 參數

```python
echo "vm.max_map_count=262144" > /etc/sysctl.conf
sysctl -p
```

```python
sysctl -p
```

> PS.剛開始會出現error
![image](https://i.imgur.com/9y7N87c.png)

等他跑一下後，
![image](https://i.imgur.com/NkyOCbE.png)

就可以成功啟動了~~
