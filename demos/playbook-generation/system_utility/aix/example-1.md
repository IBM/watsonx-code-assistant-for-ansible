#### **How to access Playbook Generation?**  
Click on the **'Ansible'** icon on VS Code's Activity Bar  
Under **'Ansible Content Creator'** -> **'Get Started'**  
Under **'Create'** -> **'Playbook with Ansible Lightspeed'**

**🎯 Copy the content below and paste into the textarea.**

```yaml
Generate playbook to perform backup ( alternate disk) on AIX servers, disable facts and them perform the following tasks:
On AIX system print a debug message 'Perform backup ( Alternate Disk ) is starting.'
Run a cleanup of all existing alternate disk copies using alt_disk module with the clean action with force and register the output
Run alternate disk copy with alt_disk module using {{ target_disk }} in targets and copy action
Assert execution 'Fixing file system superblock...' in stdout output at previous task
Finally, print a message that says 'Perform backup ( Alternate Disk ) has been successfully completed.'
```

- Press **"Analyze"** to proceed.
- **Review the suggested steps for your playbook and modify as needed.** _(Prompt refinement)_
- Press **"Generate playbook"** to open a new tab file with the full playbook.

**Note:** _The feature exclusively creates **self-contained** Full Playbooks — it does not generate Ansible roles._
