# use the README.md file for requirements to build this image
# If you get stuck, the answer/ directory has the solution
# Start FROM the alpine image. You can also practice pinning to a recent version 
# (found on Docker Hub's alpine image page.) or :latest. 
# I tend to care less about FROM image pinning for CLI tools like this.
FROM alpine:latest

# Use the apk package manager to install the cmatrix package.
RUN apk add --no-cache cmatrix

# You'll want to set the ENTRYPOINT to run cmatrix when the container starts.
ENTRYPOINT ["cmatrix"]

# Let's make this image easy to run by adding a CMD instruction with some default cmatrix arguments.
# For example, -abs -C red.
CMD ["-aBs", "-C", "green"]

# The cmatrix tool needs a terminal to run, so you need to ensure docker provisions a tty.
# Always use the -it flags with this image when running the container, or you'll get a "Error opening terminal" error.

# Docker commands to build and run this image from assignment01 directory::
# docker image build -t cmatrix ./cmatrix
# docker container run -it cmatrix