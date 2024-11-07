
1. `cd packer`
2. Run `packer init config.pkr.hcl`
3. Update `credentials.pkr.hcl`
4. Update/Check following in `ubuntu-server-noble/ubuntu-server-noble.pkr.hcl`
    - node
    - vm_id
    - vm_name
    - template_description
    - iso_file
    - ssh_username
    - ssh_password

5. Update following in 
    - name
    - passwd


4. `packer validate -var-file='credentials.pkr.hcl' ubuntu-server-noble/ubuntu-server-noble.pkr.hcl`
5. `packer build -var-file='credentials.pkr.hcl' ubuntu-server-noble/ubuntu-server-noble.pkr.hcl`