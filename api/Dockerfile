FROM node:17-alpine
# 1. Above is the parent image  and is the first layer

WORKDIR /app

COPY package.json .

RUN npm install
# 2. We add the source code, copy all code into image 
# The first dot is the directory I want to copy my source code FROM
# The second dot is the path inside the image we wand to copy the source code to
COPY . .
 

#  3. Add dependencies (tells docker to run the command on the image itself being added on
# while the image is being build)
# RUN npm install 

# tells docker which port it should expose (optional)
# PORT MAPPING  
EXPOSE 4000

# 4. Run commands 
CMD ["node", "app.js"]