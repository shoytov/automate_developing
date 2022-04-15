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

docker-clean:
	docker system prune -af
