#tested on linux ubuntu

sudo nano /etc/mongod.conf

#uncomment it and write

replication:
   oplogSizeMB: 1024
   replSetName: rs0
   enableMajorityReadConcern: true
 
#ctrl+s and ctrl+x
#delete the Environment variable from

sudo nano /usr/lib/systemd/system/mongod.service
 
#then

rs.initiate()
