# Appsilon-Task-Anisble-Configuration

## Description

Configuration Management using ansible and molecule. 

## Getting Started

### Prerequisites

- Python installed >= 3.10.
- Install the dependencies listed on `requirements.txt`: Run `pip3 install -r requirements.txt`

## Running the Playbook
1. **Prepare your inventory file**: You need an inventory file that lists the machines on which you want to run the playbook. 

2. **Execute the playbook**: Run the playbook on your inventory hosts using the following command:

   ```bash
   ansible-playbook -i inventory_file playbook.yml
   ```

   Replace `inventory_file` with the path to your inventory file.
## Testing the Playbook

Useful commands to test the configuration using [Molecule](https://ansible.readthedocs.io/projects/molecule/getting-started/)

Create clean container:

```bash
molecule create
```

Executes playbook on the container:

```bash
molecule converge
```
Login in the container:

```bash
molecule login
```
Verify the configuration:

```bash
molecule verify
```
Remove the container:

```bash
molecule destroy
```

Or simply run this command to create, converge, verify and destroy the container
```bash
molecule test
```