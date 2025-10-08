To install **IntelliJ IDEA** on **Linux Mint (based on Ubuntu)**, you have several clean and easy options. Below are the most reliable methods:

---

## ✅ **Option 1: Use JetBrains Toolbox (Recommended)**

The **JetBrains Toolbox App** makes installing and managing IntelliJ IDEA (and other JetBrains IDEs) super easy.

### ▶ Step-by-step:

1. **Download JetBrains Toolbox:**

```bash
wget https://download.jetbrains.com/toolbox/jetbrains-toolbox-1.28.1.15219.tar.gz
```

> *(Check the [official site](https://www.jetbrains.com/toolbox-app/) if you want the latest version)*

2. **Extract the archive:**

```bash
tar -xzf jetbrains-toolbox-*.tar.gz
cd jetbrains-toolbox-*/
```

3. **Run the Toolbox app:**

```bash
./jetbrains-toolbox
```

4. **Install IntelliJ IDEA** through the GUI.

> You can now launch IntelliJ from your applications menu.

---

## ✅ **Option 2: Install IntelliJ IDEA via Snap (Simple CLI install)**

Linux Mint supports **Snap**, but it may be disabled by default. You can enable and install IntelliJ like this:

### ▶ 1. **Enable Snap on Linux Mint (if not already)**

```bash
sudo rm /etc/apt/preferences.d/nosnap.pref
sudo apt update
sudo apt install snapd
```

Log out and log back in.

---

### ▶ 2. **Install IntelliJ (Community Edition)**

```bash
sudo snap install intellij-idea-community --classic
```

Or for **Ultimate Edition**:

```bash
sudo snap install intellij-idea-ultimate --classic
```

Then run with:

```bash
intellij-idea-community
```

Or launch it from your app menu.

---

## ✅ **Option 3: Manual Installation (No Snap or Toolbox)**

1. **Install dependencies (Java):**

```bash
sudo apt install openjdk-17-jdk -y
```

2. **Download IntelliJ from JetBrains:**

Go to: [https://www.jetbrains.com/idea/download/](https://www.jetbrains.com/idea/download/)

Choose **Linux** > **Community** or **Ultimate**, then:

```bash
cd /opt
sudo wget https://download.jetbrains.com/idea/ideaIC-2023.3.5.tar.gz
sudo tar -xzf ideaIC-2023.3.5.tar.gz
sudo mv idea-IC-* intellij
sudo rm ideaIC-2023.3.5.tar.gz
```

3. **Run IntelliJ:**

```bash
/opt/intellij/bin/idea.sh
```

You can optionally create a launcher or desktop entry from IntelliJ’s own settings.

---

## 🧠 TIP: Java version matters!

IntelliJ IDEA runs best with Java 17 or newer:

```bash
java -version
```

If needed:

```bash
sudo apt install openjdk-21-jdk -y
```

---

## ✅ Final Thoughts

| Method            | Best for                       |
| ----------------- | ------------------------------ |
| JetBrains Toolbox | Easiest updates and management |
| Snap              | Quick and clean CLI install    |
| Manual            | Full control, no extra tools   |

Let me know if you're working in a desktop or headless/server environment – that affects how you should launch IntelliJ.
