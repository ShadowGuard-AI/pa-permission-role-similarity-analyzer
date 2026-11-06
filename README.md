# pa-permission-role-similarity-analyzer
Analyzes different roles and identifies highly similar roles as candidate pairs for the operator to judge for consolidation, to reduce complexity and administrative overhead. Similarity uses two metrics only: assigned permissions and user assignments, combined with the two weights. Two roles that both hold no permissions and no users score 1.0. Weights that do not sum to 1, a threshold outside 0 to 1, and an input with fewer than two roles are rejected at startup with exit 1. The output file must not overwrite the role definition file. - Focused on Tools for analyzing and assessing file system permissions

## Install
`git clone https://github.com/ShadowGuard-AI/pa-permission-role-similarity-analyzer`

## Usage
`python3 main.py role_definition_file [--similarity_threshold 0.7] [--permission_weight 0.5] [--user_weight 0.5] [--output_file results.json] [--log_level INFO]`

## Parameters
- `-h`: Show help message and exit
- `role_definition_file`: (required) Path to the JSON file containing role definitions. Each role maps to an object with a `permissions` list and a `users` list.
- `--similarity_threshold`: Minimum similarity score for roles to be considered similar (default: 0.7).
- `--permission_weight`: Weight for permission similarity (default: 0.5).
- `--user_weight`: Weight for user similarity (default: 0.5).
- `--output_file`: Path to the file to save the results in JSON format. If not specified, results are printed to the console.
- `--log_level`: Set the logging level (default: INFO). Choices: DEBUG, INFO, WARNING, ERROR, CRITICAL.

## License
MIT License. See LICENSE.
