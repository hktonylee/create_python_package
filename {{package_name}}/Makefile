
all: build

build: pyproject.toml requirements.txt .pre-commit-config.yaml $(wildcard src/**/*)
	python3 -m build

clean:
	rm -rf dist

upload: clean build
	twine upload --repository codeartifact dist/*

.PHONY: all clean build upload
