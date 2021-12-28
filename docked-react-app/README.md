# Docked React App

This is a docked version of the the sample react App created by the create-react-app script.

## How to run it - Method 1 (Dev Mode)

Clone this repo.

From the base folder create the "docked-app" container with:

`docker build -t docked-app:dev .`

Then, run the container with:

`docker run -it --rm -v ${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true docked-app:dev`

Open [http://localhost:3001](http://localhost:3001) to view it in the browser.

As we can see, this is a development version of the docked app. The source is attached as a volume, if you make the source any changes, the server is rebooted.

## How to run it - Method 2 (Dev Mode)

A docker-compose.yml file is present so you can have the confort of only (from the base folder of this repo):

Build the image:
`docker-compose up -d --build`

Fire up the container:
`docker-compose up -d --build`

Stop the container:
`docker-compose stop`
