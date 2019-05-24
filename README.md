SBT Docker Container With Akka Server

    docker build --rm --tag=akka .

    docker run --rm --detach --name=akka --volume="$PWD:/usr/src" akka
    docker exec --tty --interactive akka ls
    docker exec --tty --interactive akka pwd
    docker exec --tty --interactive akka sh
    docker exec --tty --interactive akka sbt new akka/akka-scala-seed.g8
    docker exec --tty --interactive akka sbt

    docker stop akka


