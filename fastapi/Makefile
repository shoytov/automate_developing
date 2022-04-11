.SILENT: install run
.PHONY: install run

install:
	python3 -m venv env
	env/bin/pip3 install --upgrade pip && env/bin/pip3 install poetry
	env/bin/poetry init
	env/bin/poetry add mypy pep8 pylint black autoflake fastapi uvicorn loguru
	env/bin/poetry install

run:
	env/bin/uvicorn app.web:app --reload 
