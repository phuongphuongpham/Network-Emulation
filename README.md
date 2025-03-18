# Network-Emulation
CSC 466 Project

1. INSTALL GNS3: Download from https://www.gns3.com/
    For Windows:
    - Run the installer and follow the setup wizard to install GNS3.
    - During installation, it will prompt you to install dependencies like Wireshark, VirtualBox, or VMware. You can choose to install them if you don't already have them.
    For macOS:
    - Open the .dmg file and drag the GNS3 icon to the Applications folder.
    - Follow the prompts to install the necessary dependencies (VirtualBox, Wireshark, etc.).

2. INSTALL GNS3 VM: https://gns3.com/software/download-vm 
    For VirtualBox:
    - After downloading the GNS3 VM file, open VirtualBox.
    - Go to File > Import Appliance, and select the .ova file you downloaded.
    - Configure the GNS3 VM:
        Click on the VM, then go to Settings.
        Allocate the recommended amount of RAM (minimum 2 GB) and set the number of CPUs.
        In Network section, ensure that Adapter 1 is enabled and set to Host-only Adapter.
        Under Name, select the host-only network that is created (if not, you may need to create one in VirtualBox).

3. Connect GNS3 to the VM
    a. In VMware or VirtualBox, start the GNS3 VM.
    b. Connect GNS3 to the GNS3 VM:
        In GNS3, go to Edit > Preferences > GNS3 VM.
        Check the box Enable the GNS3 VM.
        Select VMware or VirtualBox as the virtualization platform, depending on what you're using.
        The GNS3 VM should now be connected, and you'll be able to start adding more complex devices (routers, firewalls, etc.).

4. Test Connection
    a. Find the GNS3 VM's IP address:
        Open the GNS3 VM console in VMware or VirtualBox.
        You can find the IP by running ip addr show or ifconfig in the GNS3 VM terminal. (SHELL)
        Look for the interface with a typical IP address format like 192.168.x.x or 10.x.x.x. Usually, it would be assigned to eth0 or ens33 (network interfaces). The IP address will appear under inet (for IPv4)
    b. Ping the GNS3 VM
        Open a Terminal or Command Prompt on host machine
        Run command: ping <GNS3_VM_IP_address>
        If the ping is successful, the GNS3 VM is reachable, and the connection is working