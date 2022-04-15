.SILENT: install run clean docker-run docker-stop docker-clean
.PHONY: install run clean docker-run docker-stop docker-clean

install:
	python3.9 -m venv env
	env/bin/pip3 install --upgrade pip && env/bin/pip3 install poetry
	env/bin/poetry install

run:
	env/bin/uvicorn app.web:app --reload

docker-run:
	docker-compose up -d --build --remove-orphans

docker-stop:
	docker-compose down

clean:
	rm -rf env
	rm -rf `find . -name __pycache__`
	rm -f `find . -type f -name '*.py[co]' `
	rm -f `find . -type f -name '*~' `
	rm -f `find . -type f -name '.*~' `
	rm -rf dist *.egg-info
	rm -rf .cache
	rm -rf .pytest_cache
	rm -rf .mypy_cache
	rm -rf htmlcov
	rm -f .coverage
	rm -f .coverage.*	

docker-clean:
	docker system prune -af
