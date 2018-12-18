# k8s_course_notes
## Docker Best Practices
* aggregate multiple `run` commands together to reduce number of layers needed.
* `docker add` allows download from the Internet + uncompress from tar + `docker copy`. Use `docker copy` in general.
* avoid tagging `latest` because it doesn't get auto-updated. Tag with a version number.
* for security, `useradd -ms` a privileged user in Dockerfile (avoiding running container as the root).
* `docker-compose build` re-builds docker image as opposed to `docker-compose up`.
