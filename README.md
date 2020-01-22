# ansible_play

# YAML Help

1.  [http://yaml.org/spec/1.2/spec.html]
1.  [https://en.wikipedia.org/wiki/YAML]
1.  [https://stackoverflow.com/questions/3790454/in-yaml-how-do-i-break-a-string-over-multiple-lines]

# Usefull playbook modules

1.  ```
    set_fact:
      our_fact: Ansible Rocks!
      ansible_distribution: "{{ ansible_distribution | upper }}"
      webserver_application_path: /local/nginx
    when: ansible_distribution == 'Ubuntu'
    ```

1.  ```
    pause:
      seconds: 10
      prompt: Please check that the webserver is running, press enter to continue
    ```

1.  ```
    wait_for:
      port: 80
    ```

1.  ```
    assemble:
      src: conf.d
      dest: sshd_config
    ```

1.  ```
    add_host:
      name: centos1
      groups: adhoc_group1, adhoc_group2
    ```

1.  ```
    group_by:
      key: "custom_{{ ansible_distribution | lower }}
    ````

1.  ```
    fetch:
      src: /etc/redhat-release
      dest: /tmp/redhat-release
    ```

# Exploring Ansible Register and When

1.  ```
    command: hostname -s
    register: hostname_output
    ```

1.  ```
    command: hostname -s
    when: ( ansible_distribution == "CentOS" and ansible_distribution_major_version == "7" ) or
          ( ansible_distribution == "Ubuntu" and ansible_distribution_major_version == "16" )
    ```

1.  ```
    command: hostname -s
    when: ( ansible_distribution == "CentOS" and ansible_distribution_major_version | int >= 5 ) or
          ( ansible_distribution == "Ubuntu" and ansible_distribution_major_version | int >= 11 )
    ```

1.  ~~~
    command: hostname -s
    when: 
      - ansible_distribution == "CentOS" 
      - ansible_distribution_major_version | int >= 7
    register: command_register
    ~~~

1.  ~~~
    - name: Install Nginx Ubuntu
      apt:
        name: nginx
        update_cache: yes
        state: latest
      when: ansible_distribution == 'Ubuntu'
    ~~~
