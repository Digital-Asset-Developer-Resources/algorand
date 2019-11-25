. Ubuntu

  1.  sudo mkfs -t xfs /dev/xvdf
  2.  sudo mkdir /data
  3.  sudo mount /dev/xvdf /data
  4.  sudo chown ubuntu:ubuntu /data
  5.  mkdir /data/algorand.com
  6.  sudo ln -s /data/algorand.com /var/lib/algorand
  7.  cd /data/algorand.com/
  8.  mkdir betanetdata


. Mac

. Windows  