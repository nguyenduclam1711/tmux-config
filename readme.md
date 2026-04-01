# My Tmux Configuration

This repository stores my personal [tmux](https://github.com/tmux/tmux/wiki) configuration files. I've designed it to enhance my terminal workflow and productivity across various development environments.

## Features

*   **Clean and organized structure**: Easy for me to navigate and understand.
*   **Directly sourced plugins**: Integration of powerful extensions without a plugin manager.
*   **Custom Keybindings**: Personalized shortcuts for my common tasks.
*   **Status Bar**: An informative and visually appealing status line, using the `catppuccin` theme.

## Setup

To set up this tmux configuration on my system, I follow these steps:

1.  **Clone the repository**:
    ```sh
    git clone https://github.com/luler/.config/tmux.git ~/.config/tmux
    ```
    *(Assuming this is cloned to `~/.config/tmux`)*

2.  **Clone Plugins**:
    This configuration directly sources plugins from specific directories. I need to clone the following plugin repositories into `~/.config/tmux/plugins/`:
    ```sh
    mkdir -p ~/.config/tmux/plugins
    git clone https://github.com/catppuccin/tmux ~/.config/tmux/plugins/catppuccin
    git clone https://github.com/tmux-plugins/tmux-cpu ~/.config/tmux/plugins/tmux-cpu
    git clone https://github.com/tmux-plugins/tmux-battery ~/.config/tmux/plugins/tmux-battery
    ```

3.  **Load Configuration**:
    I launch a new tmux session or source my `tmux.conf` file (e.g., `tmux`) to apply the changes and load the plugins.

## Usage

*   **Start a new session**: `tmux new -s my_session`
*   **Attach to a session**: `tmux attach -t my_session`
*   **Detach from a session**: `Prefix` + `d`
*   **List sessions**: `tmux ls`

I can refer to the `tmux.conf` file for specific keybindings and plugin configurations.

## Configuration Details

*   **Prefix Key**: `C-a` (Ctrl+a). This overrides the default `C-b`.
*   **Terminal**: `tmux-256color` for full color support.
*   **Mouse Support**: Enabled for easy pane and window navigation.
*   **Copy Mode**: `vi` mode with `v` to begin selection and `y` to copy.
*   **History Limit**: Set to 10000 lines.

## Custom Keybindings

Here are some of the custom keybindings defined in `tmux.conf` that I use regularly:

*   `Prefix` + `|`: Split window vertically (horizontal split).
*   `Prefix` + `-`: Split window horizontally (vertical split).
*   `Prefix` + `r`: Reload `tmux.conf` file.
*   `Prefix` + `m`: Toggle zoom for the current pane.
*   `Prefix` + `h`, `j`, `k`, `l`: Navigate between panes (left, down, up, right).
*   `Prefix` + `!`: Break current pane into a new window.
*   `Prefix` + `@`: Join the hidden pane to the current window (assuming a previous `break-pane`).

## Plugins

This configuration directly sources the following plugins by running their scripts from the `~/.config/tmux/plugins/` directory:

*   [`catppuccin/tmux`](https://github.com/catppuccin/tmux): Provides a beautiful color theme for tmux. Currently set to `frappe` flavor with `rounded` window status style.
*   [`tmux-cpu`](https://github.com/tmux-plugins/tmux-cpu): Displays CPU usage in the status bar.
*   [`tmux-battery`](https://github.com/tmux-plugins/tmux-battery): Displays battery status in the status bar.
