java --version
cd D:/project
mkdir javaproject
cd javaproject

New-Item test.java
touch test.java
nano test.java
OR
notepad test.java

javac test.java
java test.java

```
// Java Program
class test {
    public static void main(String[] args) {
        System.out.println("Hello, World!"); 
    }
}

```

touch Dockerfile
OR
New-Item Dockerfile

```
FROM openjdk:11
WORKDIR /usr/src/app
COPY . .
RUN javac test.java
CMD ["java", "test"]
```
OR
```
FROM openjdk:8u131-jre-alpine
ENV HW_HOME=/opt/test
ADD HelloWorld.class $HW_HOME/
WORKDIR $HW_HOME
ENTRYPOINT ["java", "test"]


```
git clone https://github.com/atulkamble/DevOpsTraining2024.git
cd DevOpsTraining2024
git status
git add .
git commit -m "Added Java Code"
git push origin main
New-Item Dockerfile
notepad Dockerfile
docker images
docker build -t atuljkamble/javahelloworld .
notepad Dockerfile
docker build -t atuljkamble/javahelloworld .
docker push atuljkamble/javahelloworld
