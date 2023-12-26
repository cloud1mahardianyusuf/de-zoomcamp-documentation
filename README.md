# DE-ZoomCamp Documentation

### Reference : [DataTalks Club GitHub](https://github.com/DataTalksClub/data-engineering-zoomcamp/blob/main/README.md)

## 1- Create VM and Install Docker
  - [Create VM in GCP and Create SSH key for Passwordless Login](https://github.com/cloud1mahardianyusuf/de-zoomcamp-documentation/blob/main/Create%20VM%20on%20GCP/create%20vm%20and%20ssh%20key%20passwordless.md)
  - Install Docker
      -  (Optional) Change Docker root Directory to spesific path and specify pool internal IP
          -  Create new json file in /var/docker/daemon.json, and add this configuration to change internal Pool IP and Docker Root Directory
             ```
              {
              	"bip": "179.179.0.1/16",
              	"data-root":"/data/docker_root_dir"
              }
             ```
      -  Copy get-docker.sh file from this repo, or download it from official docker website using curl
          ```
          curl -fsSL https://get.docker.com -o get-docker.sh
          ```
      -  Run the sh file
          ```
          sudo sh get-docker.sh
          ```
      -  Check Docker CE and Docker Compose Version
## 2- Tools Installation :
  - [Ubuntu-Python-Streamlit (Still working)](#)
  - [Mage-Workflow](https://github.com/cloud1mahardianyusuf/mage-workflow)
  - [Apache-Airflow](https://github.com/cloud1mahardianyusuf/apache-airflow)
