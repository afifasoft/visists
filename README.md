#build a docker image using custom name
docker build -t abdul/simpleweb:latest .		
        # -t means tag
		# -it mean input to 
#run a docker container
docker run -it abdul/simpleweb sh		

#-p	port mapping		
docker run -p 8080:8080 abdul/simpleweb	
     

#execute on running container		
docker exec -it 619f5b12431d sh		

#type exit to come out of it		
exit		


#To run compose file
docker-compose up

#To rebuild and run
docker-compose up --build

#Launch in background
docker-compose up -d

#Stop containers
docker-compose down

#Restart Policies
"no"
    #we will put quots in no only either double or single because in yml file no means false
    #Never attempt to restart this. container if it stops or crashes
always
    #If this container stops *for any reason* always attempt to restart it
on-failure
    #Only restart if the container stops with an error code
unless-stopped
    #Always restart unless we(the developers) forcibly stop it

#Container status
docker-compose ps
