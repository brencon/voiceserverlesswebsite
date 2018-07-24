# AWS Cloud9

## Installing Hugo

To install Hugo on CentOS, Red Hat Linux you may use yum. First you have to add the repository by creating a file in /etc/yum.repos.d/ and add the following content in it. You may need root access.

`vi /etc/yum.repos.d/CentOS-hugo.repo`

```
[daftaupe-hugo]
name=Copr repo for hugo owned by daftaupe
baseurl=https://copr-be.cloud.fedoraproject.org/results/daftaupe/hugo/epel-7-$basearch/
type=rpm-md
skip_if_unavailable=True
gpgcheck=1
gpgkey=https://copr-be.cloud.fedoraproject.org/results/daftaupe/hugo/pubkey.gpg
repo_gpgcheck=0
enabled=1
enabled_metadata=1
```

Now you may install Hugo using yum

`yum install hugo`

Reference: https://www.opentechguides.com/how-to/article/hugo/163/installing-hugo.html

## Starting the Hugo Site

`hugo serve --bind=0.0.0.0 -p 8080 -b https://9117c822c56f45fcb97e27a13abfa6de.vfs.cloud9.us-east-1.amazonaws.com --appendPort=false --disableFastRender`