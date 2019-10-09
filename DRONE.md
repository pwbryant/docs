### Drone CI/CD

#### Setup
* Provision medium EC2 instance (name: ci-cd)
* Update OAuth app on github with ci-cd public DNS
* Update .ssh/config drone-control ip address
* Add ci-cd instance ip to `hosts` on ansible-drone EC2
* Add ansible-drone public key to ci-cd root user's `authorized_keys` 
* Test ansible can contact ci-cd with `ansible -m ping drone_ci`
* Run `ansible-playbook role_playbook.yml -l drone_ci`
* Add access via port 80 to ci-cd security group
* Go to ci-cd public dns and activate repo of interest
* Set repo to 'Trusted' in settings
* Add docker_password and docker_username secrets
* create .drone.yml file
