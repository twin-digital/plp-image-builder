# Image Builder

Pipeline platform component for building OCI container images.

## TODO

- Enable fuse
  - Need in devcontainer (might require reconfiguring Docker host vm)
  - ENV BUILDKITD_FLAGS="--oci-worker-no-process-sandbox" -> ENV BUILDKITD_FLAGS="--oci-worker-no-process-sandbox --oci-worker-snapshotter=fuse-overlayfs"
  - Remove `--cap-add SYS_ADMIN` and add `--device /dev/fuse`
- Change to buildkit-rootless (were having issues with rootlesskit)
- Consider changing to buildah, since we avoided that simply because of fuse requirement...
