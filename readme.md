1. Link github repo: https://github.com/lam-phanminh/End-Project-1 
   ![](./github-repo.png) 
    - In this repo, I add Dockerfile to build source code PHP.
    - About Dockerfile: 

     ![](./Pictures/Dockerfile.png)

   - Base image: ```devopsedu/webapp```
   - My workdir is ``/var/www/html``
   - I add line `` DirectoryIndex  index.php `` into ``000-default.conf`` file and copy ``000-default.conf`` from this directory to `` /etc/apache2/sites-enabled/ `` of container.
   - Copy source code to `` /var/www/html `` 
   - Expose port 80 
   - Final, start apache. 
  
2. Create Jenkins pipeline job and config: 
   
    ![](./Pictures/SCM.png) 
    ![](./Pictures/Script-path.png) 

    - Job: 

    ![](./Pictures/job.png)

3. Jenkinsfile: 

   ![](./Pictures/Jenkinsfile.png)

4. Ansible:
   -  ``Playbook``: 
  
    ![](./Pictures/playbook.png)

   - ``Inventory``: 
  
    ![](./Pictures/inventory.png)

5. Console output: 
   - Stage ``Checkout...``:
  
    ![](./Pictures/Stage-checkout.png)

   - Stage ``Build......``: 
  
    ![](./Pictures/stage-build-Dockerfile.png)
    ![](./Pictures/build-dockerfile-done.png)

   - Stage ``Docker login && push image ......`` 

    ![](./Pictures/login%26push.png)
    ![](./Pictures/push-done.png)

   - Stage `` Deploy... `` 
  
    ![](./Pictures/Stage-Deploy.png)
    ![](./Pictures/deploy-done.png)

   - ``Log ansible:`` 
  
    ![](./Pictures/log-ansible.png)

6. ``Image pushed to dockerhub:``
   
   ![](./Pictures/docker-hub.png)

7. ``Container run:``
   
   ![](./Pictures/container-run.png) 

8. ``Web built:`` 

   ![](./Pictures/web-built.png)

****