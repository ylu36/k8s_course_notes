# k8s_course_notes
## Docker Best Practices
* aggregate multiple `run` commands together to reduce number of layers needed.
* `docker add` allows download from the Internet + uncompress from tar + `docker copy`. Use `docker copy` in general.
* avoid tagging `latest` because it doesn't get auto-updated. Tag with a version number.
* for security, `useradd -ms` a privileged user in Dockerfile (avoiding running container as the root).
* `docker-compose build` re-builds docker image as opposed to `docker-compose up`.
## Kubectl Basics
* `kubectl apply -f deployment.yaml` to create or update resources based on `deployment.yaml`.
* `kubectl describe pod <pod_name>` for details on one pod.
* `kubectl expose` exposes a port for deployment.
* `kubectl port-forward` forwards one or more local ports to remote pod.
* `kubectl exec -it <pod_name> bash`
* kube master(s) manages kube nodes/minions
