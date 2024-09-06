# Build Command
# docker build -t demo .

# Run Command
# docker run -it demo
# docker run -it -e API_URL="https://api.myurl.com/api" -e AUTH_CALLBACK_URL="https://my.url.com" demo

FROM ubuntu:20.04

# ###################################################################
# Environment Variables. 
# You can define envionment variables using any of the formats below. 
# ###################################################################

# ENV API_URL "http://localhost:44100"
# ENV AUTH_CALLBACK_URL "http://localhost:44300"

# ENV API_URL="http://localhost:44100"
# ENV AUTH_CALLBACK_URL="http://localhost:44300"
# note - this is the prefferred format

ENV API_URL http://localhost:44100
ENV AUTH_CALLBACK_URL http://localhost:44300
# note - this is the legacy foramt

WORKDIR /build

COPY . .

# This works to output the environment variables 
# CMD echo "API_URL, $API_URL, AUTH_CALLBACK_URL, $AUTH_CALLBACK_URL" 

# This works to output the configuration 
# CMD cat src/assets/app.dev.config.json

# Lauch the app using the docker-launch.sh script
CMD ["./docker-launch.sh"]

# ###################################################################
# Differnt ways of executing commands in Dockerfile
# You can use Shell Form or Exec Form to execute commands in Dockerfile 
# ###################################################################

# # CMD Instruction
# CMD ["echo", "Hello world"] # Exec Form
# CMD echo "Hello world"      # Shell Form

# # ENTRYPOINT Instruction
# ENTRYPOINT ["echo", "Hello world"] # Exec Form
# ENTRYPOINT echo "Hello world"      # Shell Form
