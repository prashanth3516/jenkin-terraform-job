# jenkin-terraform-job

This project creates **two files** and **two directories** using Terraform via a jenkins pipeline

---

### structure

- 'main.tf' - terraform code to create files/directories using 'local_file' resources
- 'jenkinsfile' - CI pipeline to run terrafor stages ('init', 'validate', 'plan', 'apply')

---

### how to use

1.connect this repo to jenkins (Pipeline script from scm)
2.Run the pipeline
3.check jenkins workspace - it will conatin:
     ---
     file1.txt
     file2.txt
     dir1/.placeholder
     dir2/.placeholder
     ---

---
