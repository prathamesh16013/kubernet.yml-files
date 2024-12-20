# kubernet-files
different files on kubernets .yml codes


* nfs.yml
create an efs
add sg of worker node in sg of efs at protocol NFS
create a directory on WN as myvolume
sudo apt-get update
sudo apt-get install nfs-common -y
copy mount command from efs--> attach
run that command on WN with replacing efs from command - ~/myvolume
eg: sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport fs-04afa8ea9234b32d1.efs.ap-south-1.amazonaws.com:/ ~/myvolume
go inside the myvolume and create a directory test
sudo mkdir test
cd test
sudo nano index.html
