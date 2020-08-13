filesystem
=========

    Partition, make fs and mount


Role Variables
--------------

    filesystem:
        - { dev:        [required] path to device
            fs:         [required] filesystem type
            path:       [required] mount point
            }

Example Playbook
----------------

    - hosts: servers
      vars:
        filesystem:
            - { dev: /dev/vdb, fs: btrfs,    path: '/mnt/btrfs'    }
            - { dev: /dev/vdc, fs: ext2,     path: '/mnt/ext2'     }
            - { dev: /dev/vdd, fs: ext3,     path: '/mnt/ext3'     }
            - { dev: /dev/vde, fs: ext4,     path: '/mnt/ext4'     }
            - { dev: /dev/vdf, fs: ext4dev,  path: '/mnt/ext4dev'  }
            - { dev: /dev/vdg, fs: f2fs,     path: '/mnt/f2fs'     }
            - { dev: /dev/vdh, fs: lvm,      path: '/mnt/lvm'      }
            - { dev: /dev/vdi, fs: ocfs2,    path: '/mnt/ocfs2'    }
            - { dev: /dev/vdj, fs: reiserfs, path: '/mnt/reiserfs' }
            - { dev: /dev/vdk, fs: xfs,      path: '/mnt/xfs'      }
            - { dev: /dev/vdl, fs: vfat,     path: '/mnt/vfat'     }
            - { dev: /dev/vdm, fs: swap,     path: '/mnt/swap'     }
      roles:
         - { role: filesystem, become: true }

License
-------

    MIT

Author Information
------------------

    Dmitrij Petrov
