FROM ubuntu:latest
WORKDIR /app
RUN echo touch FileCreatedByExecutable.txt > Executable.sh
RUN chmod +x Executable.sh
ENTRYPOINT [ "./Executable.sh" ]
