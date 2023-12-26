# Create VM on GCP and set-up SSH-Key for Passwordless login 

### Create VM on GCP ([What is VM ?](https://cloud.google.com/learn/what-is-a-virtual-machine))
  1. Create account on Google Cloud Platform / GCP ([you can go to this link](#))
  2. Go to GCP console<br />
    <img src="images/1. Click Console Console.png" height="50" />
    
  3. Go to Navigation menu at the top left three lines, and choose Compute Engine and then choose VM Instances.<br />
    <img src="images/2. Go to VM Intances.png" height="50" />
    
  4. Choose create instance, for creating new VM.<br />
    <img src="images/3. Create VM Instance.png" height="50" />
    
      - Name your instance
      - Choose your prefered region and zones
          - I choose asia-southeast2 (Jakarta) and detaulf zone, because I'm from Indonesia and I want to get low latency or fast response when access the VM from my laptop.<br />
            <img src="images/4. Naming VM and Choose Region.png" height="50" />
            
      - Choose your prefered machine type
          - I choose ***preset e2-standard-4*** with 4 CPU and 16 GB RAM. Because I need to install my tools on 1 VM.<br />
            <img src="images/5. Choose Machine Type.png" height="50" />
            
      - Choose your prefered Operation System (OS) and prefered size for OS disk
          - I choose Ubuntu 22.04, because Ubuntu has huge community that can help for troubleshooting.
          - I choose 10 GB disk because for OS only. But if you want to install tools on the same disk with OS, you need more than 10 GB, maybe like 50 GB.<br />
            <img src="images/6. Choose OS.png" height="50" />
            
      - Choose firewall to allow access from HTTP and HTTPS.<br />
        <img src="images/7. Choose allw access for HTTP and HTTPS.png" height="50" />
      - (Optional)
          - Add new disk, so that all of my tools are installed will be different from the OS disk. I add another 50 GB disk.<br />
            <img src="images/8. Add New Disk.png" height="50" /><br />
            <img src="images/9a. Detail add new Disk -1.png" height="50" /><br />
            <img src="images/9a. Detail add new Disk -2.png" height="50" />
          -  [Mounting new disk to Directory](https://github.com/cloud1mahardianyusuf/de-zoomcamp-documentation/blob/main/Create%20VM%20on%20GCP/Format%20disk%20and%20mount%20to%20directory.md)
            
### Set up SSH-key for passwordless login
  5. Create private key and public key using tools MobaXTerm (putty alternative)
      -  Download the Software [MobaXTerm](https://mobaxterm.mobatek.net/download.html) Free
      -  Install and open the MobaXterm, choose Menu Tools --> MobaKeyGen (SSH key Generator)<br />
        <img src="images/10. MobaXTerm Keygen.png" height="50" />
        
      -  Generate key<br />
        <img src="images/11. Generate key.png" height="50" />
        
      -  Save private key to your prefered directory<br />
        <img src="images/12. Save Public and Private key in the local directory.png" height="50" />
        
      -  Set "Key Comment" to your prefered user, for this case I'm using "root" user, and Copy the public key<br />
        <img src="images/13. Copy Public Key.png" height="50" />        
     
  6. Add Public key to VM - GCP
      -  Go to your VM on GCP, and choose edit Instance<br />
        <img src="images/14. Choose your VM.png" height="50" /><br />
        <img src="images/15. Edit VM.png" height="50" />
        
      -  Look for SSH keys part, "ADD ITEM", paste the public key and then press "enter"<br />
        <img src="images/16. Paste public Key into VM.png" height="50" />
        
  7. Connect to VM - GCP with [VS-Code](https://code.visualstudio.com/) using private - public key
      -  Add Extension SSH FS<br />
        <img src="images/17. Install VS Code Extension for Remote SSH.png" height="50" />
        
      -  Check your VM Public IP<br />
        <img src="images/18. Check Public IP for your VM.png" height="50" />
        
      -  SetUp Config SSH for your VM - GCP<br />
        <img src="images/19a. Setting Credentials for SSH to your VM.png" height="50" /><br />
        <img src="images/19b. Setting Credentials for SSH to your VM.png" height="50" />
        
      -  Connect SSH<br />
        <img src="images/20. Connect SSH.png" height="50" />
        
      -  Open Terminal SSH and Happy Coding<br />
        <img src="images/21. Open terminal and Directory SSH.png" height="50" />
