# Create VM on GCP and set-up SSH-Key for Passwordless login
  1. Create account on Google Cloud Platform / GCP ([you can go to this link](#))
  2. Go to GCP console<br />
    <img src="" height="50" />
    
  3. Go to Navigation menu at the top left three lines, and choose Compute Engine and then choose VM Instances<br />
    <img src="" height="50" />
    
  4. Choose create instance, for creating new VM. ([What is VM ?](https://cloud.google.com/learn/what-is-a-virtual-machine))
    <img src="" height="50" />
    
      - Name your instance
      - Choose your prefered region and zones
          - I choose asia-southeast2 (Jakarta) and detaulf zone, because I'm from Indonesia and I want to get low latency or fast response when access the VM from my laptop.
            
      - Choose your prefered machine type
          - I choose ***preset e2-standard-4*** with 4 CPU and 16 GB RAM. Because I need to install my tools on 1 VM.
            
      - Choose your prefered Operation System (OS) for your instance
          - I choose Ubuntu 22.04, and prefered disk size for OS, because Ubuntu has huge community that can help for troubleshooting.
          - I choose 10 GB disk because for OS only. But if you want to install tools on the same disk with OS, you need more thatn 10 GB, maybe like 50 GB.
            
      - Choose firewall to allow access from HTTP and HTTPS
      - (Optional)
          - Add new disk, so that all of my tools are installed will be different from the OS disk. I add another 50 GB disk.
            
  5. a
     
