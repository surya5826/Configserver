node {
stage("Git Clone"){

git branch: 'main', url: 'https://github.com/surya5826/Configserver.git'
}
stage("Docker build"){ 
 sh 'docker build -t configserver:latest .'
sh 'docker images'
stage("Deploy"){
 sh 'docker rm -f configserver||true' 
sh ' docker run -d -p 8888:8888 --name configserver configserver:latest'
}
}
}
