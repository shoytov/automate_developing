.SILENT: install run clean
.PHONY: install run clean

install:
	python3.9 -m venv env
	env/bin/pip3 install --upgrade pip && env/bin/pip3 install poetry
	env/bin/poetry install

run:
	env/bin/uvicorn app.web:app --reload 

clean:
	rm -rf env
