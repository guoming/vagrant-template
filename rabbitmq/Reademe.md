# Rabbitmq

## 查看集群状态
``` sh
    rabbitmqctl cluster_status
```

## 加入集群
``` sh
      sudo rabbitmqctl stop_app      
      sudo rabbitmqctl join_cluster rabbit@rabbitmq-node1 --ram
      sudo rabbitmqctl start_app
```

## 修改节点类型
``` sh
    sudo rabbitmqctl stop_app    
    sudo rabbitmqctl -n rabbit@rabbitmq-node3 change_cluster_node_type ram
    sudo rabbitmqctl start_app
```

## 离开集群
``` sh
    sudo rabbitmqctl stop_app
    sudo rabbitmqctl reset 

    sudo rabbitmqctl forget_cluster_node -n rabbit@rabbitmq-node3
    sudo rabbitmqctl start_app
```