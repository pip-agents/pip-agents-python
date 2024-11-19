init:
	pip install -r requirements.txt
    
clean:
	rm -rf .cache
	rm -rf build
	rm -rf pip_agents_core.egg-info
	rm -f pip_agents_core/*.pyc
	rm -f pip_agents_core/**/*.pyc
	rm -rf test/__pycache__
	rm -rf test/**/__pycache__
	
install:
	pip install -e .

.PHONY: test
test:
	py.test test -s

docgen:
	rm -rf build/doc
	sphinx-apidoc -f -e -o build pip_agents_core
	mv build/modules.rst build/index.rst
	sphinx-build -b html build/doc doc/api -c .
	rm -rf build
	
