project('lightbig', 'c', version : '0.1', default_options : ['warning_level=3'])

cc = meson.get_compiler('c')
m_dep = cc.find_library('m', required : true)

liblightbig = static_library('lightbig', 'src/lightbig.c')
test_lightssl = executable('test_lightbig', 'src/test_lightbig.c',
  link_with: [liblightbig], dependencies: m_dep, install: true)

test('big', test_lightssl)
