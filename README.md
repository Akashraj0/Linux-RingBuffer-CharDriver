# Linux-RingBuffer-CharDriver

A loadable Linux kernel character device driver (`/dev/myfifo`) implementing a thread-safe circular (ring) buffer with blocking I/O, `poll`/`epoll` support, `ioctl` configuration, and `debugfs` observability.

## Project Milestones
- **Phase 1:** Basic loadable kernel module (`hello.ko`), module parameters, and `kbuild` workflow (`phases/phase1-hello-module/`)
- **Phase 2:** Character device registration (`cdev`, `alloc_chrdev_region`, `device_create`)
- **Phase 3:** Ring buffer implementation & mutex synchronization
- **Phase 4:** Blocking reads/writes via wait queues & `O_NONBLOCK` support
- **Phase 5:** `poll`/`epoll` multiplexing & `ioctl` control commands
- **Phase 6:** `debugfs` runtime metrics & safe module unload handling
