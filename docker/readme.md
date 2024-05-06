This container hosts a built version of mineos.

docker run -it --rm -v $HOME/mineos:/home/mineos_user/work geodynamics/mineos

This command will start the mineos docker image and give you terminal access. Any changes made in the /home/mineos_user/work directory will be reflected on the host machine at home/mineos.
