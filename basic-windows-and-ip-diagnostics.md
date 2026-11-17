# Basic Windows and IP Diagnostics

## Commands and tools explored

### Windows Run

The Windows Run dialog can be opened with `Windows + R`. It provides a quick way to launch applications and system utilities by name.

### IP configuration

The Command Prompt command below displays basic network configuration:

```powershell
ipconfig
```

For more detailed adapter information:

```powershell
ipconfig /all
```

## Learning points

- Windows includes built-in tools that help technicians inspect and troubleshoot a computer.
- `ipconfig` helps identify whether a network adapter has an IP address, subnet mask and default gateway.
- A command's output should be interpreted in context; seeing an address alone does not prove that internet access is working.

## Next practice

In a personal lab, I plan to practise `ping`, `ipconfig`, `nslookup` and `tracert`, and learn what each command can and cannot tell me.

## Skills

`Windows` `Command Prompt` `Network Diagnostics`
