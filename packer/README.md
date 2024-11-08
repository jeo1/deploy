# Run guide
## ubuntu-server-noble
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
    - ssh_private_key_file

5. Update following in 
    - name
    - ssh_authorized_keys
    
4. `packer validate -var-file='credentials.pkr.hcl' ubuntu-server-noble/ubuntu-server-noble.pkr.hcl`
5. `packer build -var-file='credentials.pkr.hcl' ubuntu-server-noble/ubuntu-server-noble.pkr.hcl`


# Notes
- https://github.com/ChristianLempa/boilerplates/blob/main/packer/proxmox/ubuntu-server-noble/ubuntu-server-noble.pkr.hcl
- https://github.com/bobfraser1/packer-alpine 
    - passwords
- https://github.com/dustinrue/proxmox-packer/tree/main
- https://github.com/jbowdre/packer-proxmox-templates/
- https://developer.hashicorp.com/packer/guides/hcl/variables
    - covers passwords  
