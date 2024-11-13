
all: build

build: pyproject.toml requirements.txt .pre-commit-config.yaml $(wildcard src/**/*)
	python3 -m build

upload: build
	twine upload --repository codeartifact dist/*

.PHONY: aws_codeartifact_login
