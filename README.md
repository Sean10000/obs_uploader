# obs_uploader
alfred workflow: upload image to 'huawei cloud obs' from clipboard

## Before use this workflow：
  1. Own huawei cloud account and real-name authenticated
  2. Own access key and access secret key
  3. Obs bucket (set obs bucket to 'public read' if use it for image bed purpose)
  
### Requirements:
  1. obstutil
  2. huawei cloud ak sk
  3. obs bucket, endpoint, domain 

### Config steps:
  1. Dowload obsutil
  ```
  wget https://obs-community.obs.cn-north-1.myhuaweicloud.com/obsutil/current/obsutil_darwin_amd64.tar.gz
  tar -zxvf obsutil_darwin_amd64.tar.gz
  ```
  2. Config obsutil
  ```
  obs_folder=./obsutil_darwin_amd64_5.1.13
  chmod 755 ${obs_folder}/obsutil 
  ${obs_folder}/obsutil config -i=ak -k=sk -e=endpoint
  # test connection
  ${obs_folder}/obsutil ls
  ```
  3. Dowload and import alfred workflow
  4. Config workflow ![env](http://img1.obs.cn-east-3.myhuaweicloud.com/1589854452.png) ![obs info](http://img1.obs.cn-east-3.myhuaweicloud.com/1589854995.png)

  5. Test
  
    1. capture a picture
    2. press option + C
    3. paste a image url
  

### Execute Process
![workflow_img](http://img1.obs.cn-east-3.myhuaweicloud.com/1589855560.png)
  
