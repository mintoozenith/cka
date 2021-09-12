#BACKUP ETCD:
export ETCDCTL_API=3  --endpoints=https://127.0.0.1:2379  --cacert=/etc/kubernetes/pki/etcd/ca.crt  --cert=/etc/kubernetes/pki/etcd/server.crt  \
--key=/etc/kubernetes/pki/etcd/server.key snapshot save /opt/etcd-backup.db


## RESTORE BACKUP ETCD DB
ETCDCTL_API=3 etcdctl --endpoints=https://127.0.0.1:2379 --cacert=/etc/etcd/ca.crt --cert=/etc/etcd/etcd.crt --key=/etc/etcd/etcd.key snapshot restore firstbackup.db


##JSONPATH COMMAND to find first name of the people from a specific file:
$.prizes[?(@.year == 2014)].laureates[*].firstname




