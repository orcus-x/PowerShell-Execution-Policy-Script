
# PowerShell Execution Policy Script

This repository contains a PowerShell command to configure the execution policy for the current user. It is intended to enable users to run scripts securely by setting the execution policy to `RemoteSigned`.

## Purpose

The script sets the execution policy for the current user to `RemoteSigned`, allowing locally created scripts to run while requiring that scripts downloaded from the internet be signed by a trusted publisher.

## Script Details

### Command Used

```powershell
Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned
```

- **Scope**: `CurrentUser` ensures that the execution policy is applied only to the current user and does not affect other users on the system.
- **ExecutionPolicy**: `RemoteSigned` allows scripts that are created locally to run but requires a valid signature for scripts downloaded from the internet.

## How to Use

1. Open PowerShell with administrative privileges.
2. Copy and paste the command into the terminal.
3. Confirm the change when prompted.

### Notes

- Ensure you understand the implications of changing the execution policy on your system. This setting can affect script security.
- Use `Get-ExecutionPolicy -List` to view the current execution policies for all scopes.

## Troubleshooting

- If you encounter issues, verify that the current PowerShell session is running with sufficient permissions.
- To reset the execution policy, use:
  ```powershell
  Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Undefined
  ```

## License

This script is provided under the MIT License. See `LICENSE` for details.

## Contributions

Feel free to submit issues or pull requests if you encounter any problems or have suggestions for improvements.
