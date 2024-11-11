# IBM® watsonx™ Code Assistant for Ansible Lightspeed

<img src="https://github.com/user-attachments/assets/4b415ea3-a605-4cd7-896e-ccb3eb9743c1" width="95" align="left" alt="ANSIBLE_LIGHTSPED_ICON_SVG">

**IBM® watsonx™ Code Assistant(WCA) for Red Hat® Ansible Lightspeed** demystifies the process of Ansible Playbook creation through generative AI-powered content recommendations. This repository contains sample end-to-end demos, guidelines for best prompting practices, and guidelines for model customization.

<br>

## Table of Contents

- [Introduction](#table-of-contents)
- [Single-Task Generation](#single-task-generation)
  <!-- - [DEMO: Single-Task Generation](#demo---single-task-generation) -->
- [Multi-Task Generation](#multi-task-generation)
  <!-- - [DEMO: Multi-Task Generation](#demo---multi-task-generation) -->
- [Playbook Generation](#playbook-generation)
  <!-- - [DEMO: Playbook Generation](#demo---full-playbook-generation) -->
- [Playbook Explanation](#playbook-explanation)
- [Model Customization](#model-customization)
- [Ansible Lightspeed Prompting Guide - Practical hands-on](./Prompting%20guide/IBM%20CIO%20prompting%20guide.md)
- [Questions, Bug(Issue) or New Features(Contribute)](#question-bugissue--or-new-featurescontribute-️)
- [License](#license)
- [Copyright](#copyright)

<br>

## **Single-Task Generation** 

<img src="https://github.com/user-attachments/assets/2346bd2f-db2b-4587-b2d5-6a5dbab37687" width="75" align="left" alt="single-task-png">

_IBM® watsonx™ Code Assistant for Ansible Lightspeed offers a chat-style experience that allows users to generate and explain Ansible content from single task prompts. This tool collects user prompts and returns an outline of an Ansible playbook, simplifying the process of creating and understanding Ansible content._

🚀 _**Take a look at the example GIF below to see it in action!**_ 🚀

```yaml
---
- name: Configure Database servers
  hosts: databases
  become: true

  tasks:
    - name: Install postgresql-server
```

- Move your cursor to the end of the **`- name: Install postgresql-server`** task description.
- Press **"ENTER"** to generate a suggestion.
- Press **"TAB"** to accept 👍 the suggestion.

<img src="https://github.com/user-attachments/assets/f03de63b-5f23-418d-babf-2c3d93a439d4" alt="single-task-gif">

<br>

**Check out sample playbooks to see Single-Task Generation in action**
👉 Click [**here**](./demos/single-task/) to explore the demonstrations and get hands-on experience in real-world scenarios.

<br>

## **Multi-Task Generation** 

<img src="https://github.com/user-attachments/assets/adf2b4da-8d59-47d6-bfb3-3998c0b77de5" width="75" align="left" alt="multi-task-png">

_IBM® watsonx™ Code Assistant for Ansible Lightspeed offers a chat-style experience that allows users to generate multiple tasks with a single prompt entry, by chaining multiple tasks descriptions using ampersand **(&)** sign in a YAML comment at the task level._

🚀 _**Take a look at the example GIF below to see it in action!**_ 🚀

Move your cursor to the end of the line 
  
```yaml
# Run postresql-setup command & Start and enable postgresql service & Allow the traffic
```

- Press **"ENTER"** to generate a suggestion with multiple.
- Press **"TAB"** to accept 👍 the suggestion.

<img src="https://github.com/user-attachments/assets/35a1e224-58fd-4fcd-a5e2-1fa51fdaed85" alt="multi-task-gif">

**Note:** _Generating contextually aware, accurate Ansible content suggestions saves you time and helps you create efficiently. One of Red Hat Ansible Lightspeed’s superpowers is **context.** The last task just asks to **"Allow the traffic"**, which might seem counterintuitive as an AI **"ask"**, but the Red Hat Ansible Lightspeed service is aware of the Ansible Playbook it's working in and suggests a port suggestion to open which corresponds to the default port for **PostgreSQL(5432).**_

**Check out sample playbooks to see Multi-Task Generation in action**
👉 Click [**here**](./demos/multi-task/) to explore the demonstrations and get hands-on experience in real-world scenarios.

<br>

## **Playbook Generation** 

<img src="https://github.com/user-attachments/assets/7d061158-6feb-4e24-b52b-057ca1326cda" width="120" align="left" alt="playbook-generation-png">

_Playbook generation is designed to overcome the challenges of generating Ansible content Playbooks from scratch. It leverages a chat-style experience that generates **Full Ansible Playbooks** from both **single** and **multi-task** prompts._  

_The new feature Playbook generation eases that burden by leveraging a chat-style and generative AI-powered user interface that allows users to write prompts using natural language to generate full Ansible Playbooks. Users simply input a prompt and the tool will generate a set of steps that will be needed in order to run the Playbook. Once accepted, watsonx Code Assistant for Red Hat Ansible Lightspeed will provide a **Full Ansible Playbook**._

🚀 _**Take a look at the example GIF below to see it in action!**_ 🚀

**How to access Playbook Generation?**  
Click on the **'Ansible'** icon on VS Code's Activity Bar  
Under **'Ansible Content Creator'** -> **'Get Started'**  
Under **'Create'** -> **'Playbook with Ansible Lightspeed'**

**🎯 Copy the content below and paste into the textarea.**
  
```yaml
Install and enable PostgreSQL
```

- Press **"Analyze"** to proceed.
- **Review the suggested steps for your playbook and modify as needed.** _(Prompt refinement)_
- Press **"Generate playbook"** to open a new tab file with the full playbook.

<img src="./Media/playbook-generation.gif">

**Note:** _The feature exclusively creates **self-contained** Full Playbooks — it does not generate Ansible roles._

**Check out sample playbooks to see Full Playbook Generation in action**
👉 Click [**here**](./demos/playbook-generation/) to explore the demonstrations and get hands-on experience in real-world scenarios.

<br>

## **Playbook Explanation**

_Playbook explanation is designed to overcome the challenges of understanding complex Playbooks._  

_users can acquire explanations of each Playbook including a detailed summary of what the Playbook is doing, the perquisites for running the Playbook and a description of each task._

This ensures that each development team member — regardless of expertise — can understand each task and Playbook efficiently to help minimize the learning curve for faster automation content creation.

With Playbook explanation, developers can get AI-generated explanations with the click of a button. This includes a summary of the Playbook and a description of each task to better understand what the Playbook is doing. 

This especially helps to:

- **Reduce the knowledge gap:** with a chat-style experience and real-time explanation of Ansible content, developers without deep Ansible expertise can quickly learn what the code is doing to accelerate content creation or automation efforts  
- **Free up your senior subject matter experts:** for simpler Ansible content creation, developers can leverage the playbook generation feature to generate syntactically correct content recommendations faster. This allows them to focus their time on more complex work.  
- **Increase Ansible Playbook understanding:** explanation helps to understand new and existing Ansible Playbooks faster, saving developers time to focus on more critical tasks and accelerate their productivity for future maintainability.  

**How to access Playbook Explanation?**  
There are 2 ways you can initiate Playbook explanation:  
Right click on the **Playbook** -> **'Explain the playbook with Ansible Lightspeed'**  
Click on the **'Ansible'** icon on VS Code's Activity Bar -> Under **'Ansible Lightspeed'** -> **'Explain the current playbook'**  

<img src="./Media/playbook-explanation.gif">  

❗ **Note:** ❗
- _You can run playbook explanation on any existing Ansible playbooks._ 
- _Playbook explanations are strictly limited to self-contained Full Playbooks—they do not cover task files or role files._

**Video by [Anshul Behl](https://www.linkedin.com/in/ianshulbehl/) Principal Technical Marketing Manager by Red Hat®** 👇  
🎥 [Playbook Generation using Ansible Lightspeed with IBM watsonx Code Assistant](https://youtu.be/oS7mSykl_D0?list=PLdu06OJoEf2bVLR899FuKc3AiuJvbIRZU)

**Video by [Ian Smalley](https://www.linkedin.com/in/ian-smalley-3932a21b/) Editor by IBM® Technology** 👇  
🎥 [Ansible Playbook Creation with IBM watsonx Code Assistant](https://youtu.be/vG54TKeEwP4)

<br>

## **Model Customization** 

<img src="https://github.com/user-attachments/assets/3c940bed-0ed6-4afe-8380-aec5b2755642" width="75" align="left" alt="model-customization-png">

As a customer grows their Ansible Content library (or when IBM releases and updated base model), It makes sense to re-tune.

Since every organization is different, **watsonx Code Assistant for Red Hat Ansible Lightspeed** allows users to customize the AI model with their existing Ansible data. This helps provide personalized content recommendations that are more accurate and a better fit for your business.  

Model Customization is done using **Prompt Tuning:** Empowers organizations to tune its domain-specific LLM with their own Ansible data  

- **Model customization empowers organizations to tune its domain-specific LLM with their own Ansible data**
- **Customization is beneficial for Ansible because of the many modules that might exist within an Ansible Playbook**
- **Discovery of unique modules increases quality code recommendations based on organization’s preferences**

<img src="https://github.com/user-attachments/assets/c5d497ac-425b-4494-9a83-9e981285eb6a" alt="model-customization-example-png">

**NOTE:** _You don't need to be a data scientist to effectively use watsonx Code Assistant. The UI provides helpful contextual information and guidance along the way._


## **Questions❓ or issues with the documentation?** 🙋‍♂️

<!-- Questions can be useful but optional, this gives you a place to say, "This is how to contact this project maintainers or create PRs -->
If you have any questions or issues with the documentation, or if there's something you'd like to add here then you can create a new issue [**> Click Here <**](https://github.com/IBM/watsonx-code-assistant-for-ansible/issues/)

## 📝 **License** 📝
[Apache License 2.0](http://www.apache.org/licenses/)


#### **Copyright**
©️ Copyright IBM Corporation 2024
