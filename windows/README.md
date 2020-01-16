# Installing Ansible for Windows References

1.  [Manage Windows like Linux with Ansible Video](https://www.youtube.com/watch?v=FEdXUv02Dbg)
2.  [AnsibleDocs-Windows Guides](https://docs.ansible.com/ansible/latest/user_guide/windows.html)
3.  [AnsibleDocs-FAQ](https://docs.ansible.com/ansible/latest/reference_appendices/faq.html)
4.  [AnsibleDocs-Windows Modules](https://docs.ansible.com/ansible/latest/modules/list_of_windows_modules.html)
5.  [JeffGeerling-Using Ansible through Windows 10's Subsystem for Linux](https://www.jeffgeerling.com/blog/2017/using-ansible-through-windows-10s-subsystem-linux)
6.  [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about)
7.  [Ansible-Windows Host Setup](https://docs.ansible.com/ansible/latest/user_guide/windows_setup.html#)
8.  [ConfigureRemotingForAnsible.ps1](https://github.com/ansible/ansible/blob/devel/examples/scripts/ConfigureRemotingForAnsible.ps1)

# Example Ansible commands, using Ubuntu on WSL:
1.  ansible-playbook Playbook1.yml -i inventory.txt --connection=local
2.  ansible-playbook test.yml -i inventory.txt --connection=local
