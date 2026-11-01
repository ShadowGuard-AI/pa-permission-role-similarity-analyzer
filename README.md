# pa-permission-role-similarity-analyzer
Analyzes different roles and identifies highly similar roles as candidate pairs for the operator to judge for consolidation, to reduce complexity and administrative overhead. Similarity uses two metrics only: assigned permissions and user assignments, combined with the two weights. Two roles that both hold no permissions and no users score 1.0. Weights that do not sum to 1, a threshold outside 0 to 1, and an input with fewer than two roles are rejected at startup with exit 1. The output file must not overwrite the role definition file. - Focused on Tools for analyzing and assessing file system permissions

## Install
`git clone https://github.com/ShadowGuardAI/pa-permission-role-similarity-analyzer`

## Usage
`./pa-permission-role-similarity-analyzer [params]`

## Parameters
- `-h`: Show help message and exit
- `--similarity_threshold`: No description provided
- `--permission_weight`: No description provided
- `--user_weight`: No description provided
- `--output_file`: Path to the file to save the results in JSON format. If not specified, results are printed to the console.
- `--log_level`: No description provided

## License
Copyright (c) ShadowGuardAI
