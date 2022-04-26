- 👋 Hi, I’m @Northstarbom
- 👀 I’m interested in ... Meta platforms
- 🌱 I’m currently learning ... Quantum coding
- 💞️ I’m looking to collaborate on ... Metaverse development
- 📫 How to reach me ... Bomlaqi@gmail.com

<!---
Northstarbom/Northstarbom is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

name: first North

git clone https://github.com/diem/my-first-client.git


PHONY: java python typescript

help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

all: java python

java: ## Build and execute all the Java code samples
# verify java version is 1.8
ifeq ($(shell java -version 2>&1 | grep "1.8" >/dev/null; printf $$?),0)
	@echo "Found correct java version"
else
	$(error "Could not find correct java version, please install 1.8")
endif

#verify gradle version is 5+
	@test "$(shell gradle -v | grep Gradle | grep -o '[0-9]\+.[0-9]\+.[0-9]\+' | head -c 1)" -ge 5 || (echo "Could not find correct gradle version, please install 5+"; exit 13)
	@echo Found correct gradle version

	cd java/; ./make-java.sh

python: ## Install and execute all the Python examples
# verify python version
ifeq ($(shell python -V 2>&1 | grep "3.7.*" >/dev/null; printf $$?),0)
	@echo "Found correct python version"
else
	$(error "Could not find correct python version, please install 3.7.7")
endif

# verify pipenv existence
ifeq (, $(shell which pipenv))
	$(error "Please install pipenv")
endif

	@cd python/; ./make-python.sh

typescript:
	@echo "typescript"
