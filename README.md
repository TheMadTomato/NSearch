# nsearch - NSE Script Search Tool

**nsearch** is a lightweight tool designed to help users quickly find specific Nmap Scripting Engine (NSE) scripts on their system. It searches through the NSE script directory and filters the list based on the given input.

## How It Works

`nsearch` is short for **NSE search**. It searches for NSE scripts stored in `/usr/share/nmap/scripts` and allows users to filter results using `grep`. This is especially useful when you're looking for specific scripts without having to manually navigate through the entire list.

## Installation

### Fish Shell

To use `nsearch` in Fish, add the following function to your `config.fish`:

```fish
function nsearch
    ls /usr/share/nmap/scripts | grep -e $argv
end
```

### Bash Shell 

To use `nsearch` in Bash, add the following function to your `.bashrc`:

```bash 
function nsearch() {
    ls /usr/share/nmap/scripts | grep -e "$@"
}

```

After saving the file, reload your shell configuration:
```bash 
source ~/.bashrc
```

### Zsh Shell 
To use `nsearch` in Zsh, add the following function to your `.zshrc`:

```zsh
nsearch() {
    ls /usr/share/nmap/scripts | grep -e "$@"
}
```

After saving the file, reload your shell configuration:
```zsh 
source ~/.zshrc
```

## Usage
Once you have installed `nsearch`, you can use it to search through the NSE scripts with any keyword. For example, to search for scripts related to "http":
```bash 
nsearch http

```
This will return all NSE scripts related to "http" from the `/usr/share/nmap/scripts` directory.

--- 
All Credits goes to the amazing Nmap team for having such an amazing tool. My utility is nothing but an ezier way to search through the many NSE scripts.

