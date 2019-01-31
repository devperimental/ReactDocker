# ReactDocker
React in Docker

	a -> Install Yarn 1.13
		https://yarnpkg.com/lang/en/docs/install/#windows-stable

	b -> create-react-app
		https://facebook.github.io/create-react-app/docs/getting-started
		
		yarn create-react-app react-app
		yarn start
		yarn build
		
	c -> create Dockerfile 
	d -> create .dockerignore

	e -> build image
		docker build . -t architectednet/react-docker

	f -> run container
		docker run -p 8000:80 architectednet/react-docker -name react-container

