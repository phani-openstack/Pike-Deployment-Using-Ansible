# Install openstack pike use ansible 2.4 on ubuntu 16.04.3 with openvswitch 2.8
# openstack pike ansible


   ssh-keygen
 
   ssh-copy-id root@controller 
 
   ...
 
   hosts
   group_vars/all
 
   openstack pike
      
   - networking-sfc
   - mistral
   - ceilometer  
   - networking-sfc-compute
   - ceilometer-compute   #There are problems with installation
   

   bash cmd_deploy 
   
   ansible all -m shell -a timedatectl
  
 
      ansible-playbook -i hosts deploy_pike.yml --tags=sshauth
      
      ansible-playbook -i hosts deploy_pike.yml --tags=common
      
 phani.openstack@gmail.com
