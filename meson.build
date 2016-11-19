project('avian', ['cpp'])

subdir('classpath')

javac = find_program('javac')

classpath_classes = custom_target('classpath_classes',
  input: classpath_java_sources,
  output: 'classpath_classes',
  capture: true,
  command: [javac,
    '-encoding', 'UTF-8',
    '-source', '1.6', # JAVA_VERSION,
    '-target', '1.6', # JAVA_VERSION,
    '-d', meson.current_build_dir() + '/classpath',
    '-bootclasspath', meson.current_build_dir() + '/classpath',
    '@INPUT@'
  ],
)
