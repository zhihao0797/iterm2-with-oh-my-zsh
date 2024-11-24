### **Install Oh My Zsh and Configure on macOS with iTerm2**

---

### **1. Install iTerm2**
- Download iTerm2 from [iTerm2 Official Website](https://iterm2.com/).
- Optionally, set it as the default terminal: Preferences → General → "Make iTerm2 Default Term".

---

### **2. Install Zsh**
- Zsh is pre-installed on macOS. To upgrade:
  ```bash
  brew install zsh
  ```
- Verify installation:
  ```bash
  zsh --version
  ```
- Set Zsh as the default shell:
  ```bash
  chsh -s $(which zsh)
  ```
- Restart iTerm2.

---

### **3. Install Oh My Zsh**
- Run the following command:
  ```bash
  sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```

---

### **4. Install Plugins**
- Open the configuration file:
  ```bash
  nano ~/.zshrc
  ```
- Add plugins:
  ```bash
  plugins=(git z zsh-autosuggestions zsh-syntax-highlighting)
  ```

#### Install additional plugins:
- **zsh-autosuggestions**:
  ```bash
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```
- **zsh-syntax-highlighting**:
  ```bash
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```

---

### **5. Install Powerlevel10k**
- Clone the theme:
  ```bash
  git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
  ```
- Set the theme:
  ```bash
  ZSH_THEME="powerlevel10k/powerlevel10k"
  ```
- Reload Zsh:
  ```bash
  source ~/.zshrc
  ```
- Configure the theme:
  ```bash
  p10k configure
  ```

---

### **6. Install Nerd Font**
- Download a Nerd Font from [Nerd Fonts](https://www.nerdfonts.com/). Recommended: **Hack Nerd Font** or **MesloLGS NF**.
- Install the font by opening the `.ttf` file.
- Set the font in iTerm2: Preferences → Profiles → Text → Change Font → Select the Nerd Font.

---

### **7. Reload Configuration**
```bash
source ~/.zshrc
```
