# Installing Ansible for Windows References

1.  [Manage Windows like Linux with Ansible Video](https://www.youtube.com/watch?v=FEdXUv02Dbg)
1.  [Ansible for the Windows Admin Video (Powershell + DevOps 2019)](https://www.youtube.com/watch?v=ZI20Y10OKd0)
1.  [AnsibleDocs-Windows Guides](https://docs.ansible.com/ansible/latest/user_guide/windows.html)
1.  [AnsibleDocs-FAQ](https://docs.ansible.com/ansible/latest/reference_appendices/faq.html)
1.  [AnsibleDocs-Windows Modules](https://docs.ansible.com/ansible/latest/modules/list_of_windows_modules.html)
1.  [JeffGeerling-Using Ansible through Windows 10's Subsystem for Linux](https://www.jeffgeerling.com/blog/2017/using-ansible-through-windows-10s-subsystem-linux)
1.  [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about)
1.  [Ansible-Windows Host Setup](https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#)
1.  [ConfigureRemotingForAnsible.ps1](https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1)
1.  [Ansible Examples - GITHUB](https://github.com/ansible/ansible-examples)

# Example Ansible commands, using Ubuntu on WSL:
1.  ansible-playbook Playbook1.yml -i inventory.txt --connection=local
1.  ansible-playbook test.yml -i inventory.txt --connection=local
1.  ansible win -i hosts -m win_ping
1.  ansible-playbook -i hosts 01_chocolatey_example.yml
1.  ansible locahost -m setup       # Displays all facts for localhost
