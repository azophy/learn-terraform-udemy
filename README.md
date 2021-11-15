REPOSITORY BELAJAR TERRAFORM DI UDEMY
=====================================

Course Link: https://www.udemy.com/share/1020rO3@noLhYsny0TyFeWElnJ3HYOjyvapKr9U4Z8innm2oRKVrJMHDrCpMW5csN8F0gJdp/

## Installation
- download file zip yg sesuai di https://www.terraform.io/downloads.html
- extract file zip. program terrafrom adalah single-executable CLI app

## 8. Understanding Terraform HCL
### Variables
- bikin folder khusus utk terraform, kasih 1 script misal "main.tf"
- contoh konten untuk terraform v1.x:
  ```
  variable "myvar" {
    type = string
    default = "hello terraform"
  }
  ```

  note: di sini type nya gak dikasih string kayak di udemy, karena di terrafrom versi baru ada notif:
  ```
  ╷
  │ Error: Invalid quoted type constraints
  │
  │   on main.tf line 2, in variable "myvar":
  │    2:   type = "string"
  │
  │ Terraform 0.11 and earlier required type constraints to be given in quotes, but
  │ that form is now deprecated and will be removed in a future version of
  │ Terraform. Remove the quotes around "string".
  ```

- variabel yg kita bikin di main.tf ini bisa diakses dari command `terraform console` -> RPL nya terraform
  - cara nyebut var dari terraform console: `var.myvar` atau `"${var.myvar}"`

- tipe variabel yang bisa dipakai:
  - string
  - map of something..
  - list
  - boolean

- `terraform console` gak autodetect perubahan file2 .tf . harus di restart manual
- variabel list bisa detect manual tipe data isi list nya
- ada fungsi2 kayak slice(), dll

### resource
- need to specify provider
