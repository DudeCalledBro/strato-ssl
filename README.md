# Strato SSL (Ansible)

This repository contains Ansible playbooks for generating certificate signing requests for Strato ssl certificates.

## Prerequisites

- Ensure you have Ansible installed (e.g. `pip3 install ansible`)

## Example

1. Copy the example variable file and name it `config.yml`

2. Define the required variables

    ```yaml
    # Set path to certificates directory
    csr_path: "{{ playbook_dir }}/certs"

    # Set list of certificates (csr)
    csr:
      - common_name: example.com
        subject_alt_name:
          - DNS:blog.example.com
    ```

3. Run the Ansible playbook

    ```bash
    ansible-playbook play-csr.yml
    ```

## License

Copyright © 2024 Niclas Spreng

Licensed under the [MIT license](LICENSE).
