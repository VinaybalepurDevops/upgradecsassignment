FROM node:12
RUN mkdir UPSTAC-Microservices-Frontend
ADD ./UPSTAC-Microservices-Frontend /UPSTAC-Microservices-Frontend
COPY ./start.sh /UPSTAC-Microservices-Frontend
WORKDIR /UPSTAC-Microservices-Frontend
RUN npm install
RUN npm build
EXPOSE 3000
RUN CI=true
RUN stdin_open=true
CMD ["npm","start"]
