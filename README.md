# tennis_pose_estimation
## WSL installation
[ref](https://learn.microsoft.com/ko-kr/windows/wsl/install)
[ref](https://learn.microsoft.com/en-us/windows/wsl/basic-commands)
[ref](https://blog.naver.com/dychoe80/222953585086)
1. open the Terminal on Windows
2. Type the command below
```
# List installed Linux distributions
> wsl --list --verbose
# default distribution
> wsl --install

# specific distro
## see the list of WSL distro available to download online
> wsl --list --online
## install
> wsl --install -d <DistroName>
> wsl --install -d Ubuntu-20.04
```
3. Check the version installed
```
1. open Ubuntu 20.04.6 LTS
2. Type the command below
$ lsb_release -a
```

## Docker Installation
[ref](https://www.docker.com/products/docker-desktop/)

## CVAT Installation
[ref](https://docs.cvat.ai/docs/administration/basics/installation/)
1. (CMD) Type the commands below
```
git clone https://github.com/opencv/cvat.git
cd cvat
docker compose up -d
# enter docker image first
docker exec -it cvat_server /bin/bash
# then run
python3 ~/manage.py createsuperuser
```
2. Open Chrome and type HTTP://localhost:8080

if you face the error "404 page not found",
[ref](https://chatgpt.com/share/09bf9b74-ae26-4ca0-86d9-f0ca8cddee34)
1. open the file "docker-compose.yml in cvat folder
2. find 8080 and change it to 8081
8080:8080 -> 8081:8080
3. Open Chrome and type HTTP://localhost:8081

## Nuclio Installation
[ref](https://docs.nuclio.io/en/stable/tasks/quick-start.html)
1. Type the command below
```(CMD)
docker run --detach --publish 8070:8070 --volume /var/run/docker.sock:/var/run/docker.sock --name nuclio-dashboard quay.io/nuclio/dashboard:stable-amd64
```
2. Browse to http://localhost:8070

## yoloV5
```
git clone https://github.com/ultralytics/yolov5.git
cd yolov5
pip install -r requirements.txt
```
```
## 모델 및 가중치 다운로드
curl -L -o models/yolov5s.pt https://github.com/ultralytics/yolov5/releases/download/v5.0/yolov5s.pt
```
