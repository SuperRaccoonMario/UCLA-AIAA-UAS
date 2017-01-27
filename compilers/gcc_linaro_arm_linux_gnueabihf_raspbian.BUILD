package(default_visibility = ['//visibility:public'])

filegroup(
  name = 'gcc',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-gcc-4.9.3',
  ],
)

filegroup(
  name = 'ar',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-ar',
  ],
)

filegroup(
  name = 'ld',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-ld',
  ],
)

filegroup(
  name = 'nm',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-nm',
  ],
)

filegroup(
  name = 'objcopy',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-objcopy',
  ],
)

filegroup(
  name = 'objdump',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-objdump',
  ],
)

filegroup(
  name = 'strip',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-strip',
  ],
)

filegroup(
  name = 'as',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-as',
  ],
)

cc_library(
  name = 'librt',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/arm-linux-gnueabihf/sysroot/usr/lib/librt.so',
  ],
)

cc_library(
  name = 'libdl',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/arm-linux-gnueabihf/sysroot/usr/lib/libdl.so',
  ],
)

cc_library(
  name = 'libm',
  srcs = [
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/arm-linux-gnueabihf/sysroot/usr/lib/libm.so',
  ],
)

cc_library(
  name = 'libpthread',
  deps = [
    '@//tools/cpp/gcc_linaro_arm_linux_gnueabihf_raspbian:libpthread',
  ],
)

filegroup(
  name = 'compiler_pieces',
  srcs = glob([
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/arm-linux-gnueabihf/**',
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/libexec/**',
    'arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/lib/gcc/arm-linux-gnueabihf/**',
  ], [
    # Exclude empty files so Bazel's caching works.
    # TODO(Brian): remove this once the Bazel bug is fixed.
    '**/.install',
  ]),
)

filegroup(
  name = 'compiler_components',
  srcs = [
    ':gcc',
    ':ar',
    ':ld',
    ':nm',
    ':objcopy',
    ':objdump',
    ':strip',
    ':as',
  ],
)
