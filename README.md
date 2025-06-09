# Calculator
simple calculator using HTML ,CSS, JavaScript
https://github.com/Mohi-th/jenkins.git

sudo apt update
sudo apt install ansible -y
nano hosts
[local]
localhost ansible_connection=local
ansible -i hosts local -m ping
nano install_nginx.yml
---
- name: Install and start NGINX on localhost
  hosts: local
  become: yes

  tasks:
    - name: Install NGINX
      apt:
        name: nginx
        state: present
        update_cache: yes

    - name: Ensure NGINX is running
      service:
        name: nginx
        state: started
        enabled: yes
ansible-playbook -i hosts install_nginx.yml


mvn archetype:generate -DgroupId=com.example -DartifactId=mavenexample -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
mvn clean install
mvn exec:java -Dexec.mainClass="com.example.App"
gradle init
gradlew build
gradlew run
