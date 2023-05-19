.PHONY: build run stop clean test help


help: ## Show this help message
	@echo "Available targets:"
	@echo "  build   - Compile the source code of the application"
	@echo "  run     - Run the application in the background"
	@echo "  stop    - Stop the application"
	@echo "  clean   - Stop the application and clean up"
	@echo "  test    - Test the application"
	@echo "  help    - Show this help message"

build: ## Compile the source code of the application
	go build -o awesome-api

run: ## Run the application in the background
	./awesome-api > ./awesome-api.log 2>&1 &

stop: ## Stop the application
	pkill awesome-api

clean: stop ## Stop the application and clean up
	rm -f awesome-api awesome-api.log

test: ## Test the application
	@echo "Testing request to http://localhost:9999"
	curl -s http://localhost:9999 || true
	@echo ""
	@echo "Testing request to http://localhost:9999/health"
	curl -s http://localhost:9999/health || true

