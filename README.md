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

```
.
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
...
├── R-batch
│   ├── Dockerfile
│   ├── dockerignore
│   └── Jenkinsfile
├── terraform
│   └── Jenkinsfile
```

## Template 구성 방법
위 예시에서는 8개의 템플릿 중 3가지만을 나타내고 있습니다. 각각 용도가 다른 템플릿이기 때문에 구조 또한 다릅니다.

### charts, Dockerfile, Jenkinsfile이 필요한 Template
개발자 분들이 가진 소스들은 대부분 해당  template을 이용하여 구성할 수 있습니다.
1. 새로운 Repository를 github 또는 private repository에 생성합니다.
1. valve-template 에서 제공하는 template 중 R-batch, terraform을 제외한 나머지 중 비슷한 성격의 template을 복사하여 새로 생성할 Repository에 copy합니다.
1. 필요한 파일들을 수정합니다. 수정해야할 요소는 다음과 같습니다.
* charts/values.yaml
* Dockerfile
* Jenkinsfile

**참고** _charts에 있는 모든 요소들은 helm을 알아야 합니다.(https://https://helm.sh)_
1. git push 하여 repository에 등록합니다.

### Dockerfile, Jenkinsfile 또는 Jenkinsfile만 필요한 Template
charts를 필요로 하지 않는 애플리케이션이 있을 수 있습니다. 해당되는 애플리케이션은 R-batch, terraform 과 같은 template을 참고하여 위와 같은 방식으로 Repository에 등록합니다.
