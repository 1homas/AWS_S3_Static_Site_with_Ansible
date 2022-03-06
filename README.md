# AWS S3 Static Site with Ansible

Deploys an AWS S3 bucket as a static web site (HTTP) using Ansible.

## Quick Start

1. Clone this repository:  

    ```bash
    git clone https://github.com/1homas/AWS_S3_Static_Site_with_Ansible.git
    ```

1. Customize any settings in the `vars.yaml` file:
   - `project_name` : use a project name to tag AWS resources for tracking and easy termination when done

2. Create your Python environment and install Ansible:  

    ```bash
    pip install --upgrade pip
    pip install pipenv
    pipenv install --python 3.9
    pipenv install ansible boto boto3 botocore
    pipenv shell
    ```

    If you have any problems installing Python or Ansible, see [Installing Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

3. Export your AWS Access & Secret keys into your terminal environment:  

    ```bash
    export AWS_REGION='us-west-1'
    export AWS_ACCESS_KEY='AKIAIOSF/EXAMPLE+KEY'
    export AWS_SECRET_KEY='wJalrXUtnFEMI/K7MDENG/bPxRfi/EXAMPLE+KEY'
    ```

    or you may source these variables from a file:

    ```bash
    source ~/.env/aws.sh
    ```

4. Run the Ansible playbook:  

    ```bash
    ansible-playbook playbook.yaml
    ```

5. When you're done, you may terminate the instances and remove all resources :

    ```bash
    ansible-playbook terminate.yaml
    ```


## License

This repository is licensed under the [MIT License](https://choosealicense.com/licenses/mit/).




