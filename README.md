# ansiblegrafana
--- 
- name: install monitoring stack
  hosts: monitorserver
  become: yes
  roles:
  - prometheus
  - grafana
- name: install node-exporter
  hosts: nodeservers
  become: yes
  roles:
  - node-exporter