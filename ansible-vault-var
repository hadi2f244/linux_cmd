#!/bin/bash
set -euo pipefail

echo "Commmand: ansible -i \"localhost,\" all  -m debug  -a 'msg=\"{{ $1 }}\"' --vault-password-file=$2 -e@$3"

ansible -i "localhost," all  -m debug  -a 'msg="{{ '$1' }}"' --vault-password-file=$2 -e@$3

if [[ $? != 0 ]]; then
    echo "Example: ansible-vault-var <var_name> <vault_pass_file> <yaml_file_path>"
fi
