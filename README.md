# valve-template

`valve`를 이용하는 개발자가 사용할 수 있는 디폴트 템플릿입니다. 
디폴트 템플릿은 총 8개를 지원하고 있습니다.

기본으로 제공된느 설정 파일은 개발 언어, 빌드 도구, 런타임 베이스 이미지에 따라 달라집니다
`valve`는 다음과 같은 설정 파일을 지원합니다.
* java-mvn-lib
* java-mvn-springboot
* java-mvn-tomcat
* js-npm-nginx
* js-npm-nodejs
* R-batch
* terraform
* web-nginx

설정 파일 유형은 <개발 언어>-<빌드 도구>-<베이스 이미지>로 명명됩니다.

디폴트 템플릿을 참고하여 자신만의 템플릿을 만들 수 있습니다.

.
├── java-mvn-lib
│   └── Jenkinsfile
├── java-mvn-springboot
│   ├── charts
│   │   └── acme
│   │       ├── Chart.yaml
│   │       ├── templates
│   │       │   ├── configmap.yaml
│   │       │   ├── deployment.yaml
│   │       │   ├── _helpers.tpl
│   │       │   ├── hpa.yaml
│   │       │   ├── ingress.yaml
│   │       │   ├── NOTES.txt
│   │       │   ├── pdb.yaml
│   │       │   ├── secret.yaml
│   │       │   └── service.yaml
│   │       └── values.yaml
│   ├── Dockerfile
│   ├── dockerignore
│   ├── draftignore
│   ├── draft.toml
│   ├── Jenkinsfile
│   └── valvesecret
├── java-mvn-tomcat
│   ├── charts
│   │   └── acme
│   │       ├── Chart.yaml
│   │       ├── templates
│   │       │   ├── configmap.yaml
│   │       │   ├── deployment.yaml
│   │       │   ├── _helpers.tpl
│   │       │   ├── hpa.yaml
│   │       │   ├── ingress.yaml
│   │       │   ├── NOTES.txt
│   │       │   ├── pdb.yaml
│   │       │   ├── secret.yaml
│   │       │   └── service.yaml
│   │       └── values.yaml
│   ├── Dockerfile
│   ├── dockerignore
│   ├── draftignore
│   ├── draft.toml
│   ├── Jenkinsfile
│   └── valvesecret
├── js-npm-nginx
│   ├── charts
│   │   └── acme
│   │       ├── Chart.yaml
│   │       ├── templates
│   │       │   ├── configmap.yaml
│   │       │   ├── deployment.yaml
│   │       │   ├── _helpers.tpl
│   │       │   ├── hpa.yaml
│   │       │   ├── ingress.yaml
│   │       │   ├── NOTES.txt
│   │       │   ├── pdb.yaml
│   │       │   ├── secret.yaml
│   │       │   └── service.yaml
│   │       └── values.yaml
│   ├── Dockerfile
│   ├── dockerignore
│   ├── draftignore
│   ├── draft.toml
│   └── Jenkinsfile
├── js-npm-nodejs
│   ├── charts
│   │   └── acme
│   │       ├── Chart.yaml
│   │       ├── templates
│   │       │   ├── configmap.yaml
│   │       │   ├── deployment.yaml
│   │       │   ├── _helpers.tpl
│   │       │   ├── hpa.yaml
│   │       │   ├── ingress.yaml
│   │       │   ├── NOTES.txt
│   │       │   ├── pdb.yaml
│   │       │   ├── secret.yaml
│   │       │   └── service.yaml
│   │       └── values.yaml
│   ├── Dockerfile
│   ├── dockerignore
│   ├── draftignore
│   ├── draft.toml
│   ├── Jenkinsfile
│   └── valvesecret
├── R-batch
│   ├── Dockerfile
│   ├── dockerignore
│   └── Jenkinsfile
├── terraform
│   └── Jenkinsfile
└── web-nginx
    ├── charts
    │   └── acme
    │       ├── Chart.yaml
    │       ├── templates
    │       │   ├── configmap.yaml
    │       │   ├── deployment.yaml
    │       │   ├── _helpers.tpl
    │       │   ├── hpa.yaml
    │       │   ├── ingress.yaml
    │       │   ├── NOTES.txt
    │       │   ├── pdb.yaml
    │       │   ├── secret.yaml
    │       │   └── service.yaml
    │       └── values.yaml
    ├── Dockerfile
    ├── dockerignore
    ├── draftignore
    ├── draft.toml
    └── Jenkinsfile
