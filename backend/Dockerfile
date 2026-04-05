# FROM node:20
# WORKDIR /opt/backend
# COPY  package.json .
# COPY *.js .
# RUN npm install 
# ENV DB_HOST="mysql"
# CMD ["node","index.js"]


# use the Minimal images only here
# IC -1
FROM node:20.18.3-alpine3.21 
# On top of IC-1 Instruction-2 is executed/ and save this layer 2 image .IC-1 is removed
RUN addgroup -S expense && adduser -S expense -G expense expense  && \
# Create IC-2 on top of IC-2 Instruction-3 is executed &Save these as layer3 image ; Ic-2 is Removed
    mkdir /opt/backend  && \
    chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package*.json ./
RUN npm install
COPY . .
ENV DB_HOST="mysql"
USER expense
CMD ["node", "index.js"]