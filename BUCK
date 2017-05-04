exported_linux_headers = {
  'jconfig.h': 'jconfig.cfg',
}

exported_macos_headers = {
  'jconfig.h': 'jconfig.cfg',
}

exported_windows_headers = {
  'jconfig.h': 'jconfig.vc',
}

cxx_library(
  name = 'jpeg',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('', '*.h'),
  ]),
  exported_platform_headers = [
    ('default', exported_linux_headers),
    ('^linux.*', exported_linux_headers),
    ('^macos.*', exported_macos_headers),
    ('^windows.*', exported_windows_headers),
  ],
  srcs = glob([
    'jcapimin.c',
    'jcapistd.c',
    'jccoefct.c',
    'jccolor.c',
    'jcdctmgr.c',
    'jchuff.c',
    'jcinit.c',
    'jcmainct.c',
    'jcmarker.c',
    'jcmaster.c',
    'jcomapi.c',
    'jcparam.c',
    'jcphuff.c',
    'jcprepct.c',
    'jcsample.c',
    'jctrans.c',
    'jdapimin.c',
    'jdapistd.c',
    'jdatadst.c',
    'jdatasrc.c',
    'jdcoefct.c',
    'jdcolor.c',
    'jddctmgr.c',
    'jdhuff.c',
    'jdinput.c',
    'jdmainct.c',
    'jdmarker.c',
    'jdmaster.c',
    'jdmerge.c',
    'jdphuff.c',
    'jdpostct.c',
    'jdsample.c',
    'jdtrans.c',
    'jerror.c',
    'jfdctflt.c',
    'jfdctfst.c',
    'jfdctint.c',
    'jidctflt.c',
    'jidctfst.c',
    'jidctint.c',
    'jidctred.c',
    'jquant1.c',
    'jquant2.c',
    'jutils.c',
    'jmemmgr.c',
    'jmemansi.c',
  ]),
  visibility = [
    'PUBLIC',
  ],
)

cxx_binary(
  name = 'example',
  srcs = [
    'example.c',
  ],
  deps = [
    ':jpeg',
  ],
)
