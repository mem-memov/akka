SBT Docker Container With Akka Server

    docker build --rm --tag=akka .

    docker run --rm --detach --name=akka --volume="$PWD:/usr/src" --user="$(id -u):$(id -g)" akka
    docker exec --tty --interactive akka ls
    docker exec --tty --interactive akka pwd
    docker exec --tty --interactive akka bash
    docker exec --tty --interactive akka ./sbt.sh new akka/akka-scala-seed.g8
    docker exec --tty --interactive akka ./sbt.sh

    docker stop akka


