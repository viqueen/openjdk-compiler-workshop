# openjdk-compiler-workshops

## getting started using docker

- clone them repos, notice the target location and the symlink, if you change one, you need to change the other

The symlink is there to help resolve IDE configurations, which we will cover in [Task 0](#task-0--ide-setup)

```bash
git clone https://github.com/openjdk/jdk.git --depth 1 ~/workshop-sources/jdk
git clone https://github.com/viqueen/openjdk-compiler-workshops.git ~/workshop-sources/openjdk-compiler-workshops

ln -sfnv ~/workshop-sources /tmp/workshop-sources
```

- compose them up

```bash
cd ~/workshop-sources/openjdk-compiler-workshops
docker compose up -d
```

- open terminal session

```bash
docker exec -it openjdk-compiler-workshops-1 bash
```

## task 0 : IDE Setup

- in the container terminal session

```bash
cd /tmp/workshop-sources/jdk
bash configure
```

- if you are using IntelliJ IDEA
```bash
bash bin/idea.sh
```

- if you are using VSCode run the command and then open `build/linux-x86_64-server-release/jdk.code-workspace` file in VSCode
```bash
make vscode-project
```


## workshop tasks

[compiler lint options: Will it run ? ... should it even compile ?](compiler-lint-options/README.md)
