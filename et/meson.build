et_inc = include_directories('.')

# Target dependency -------------------------------------------------------------------------

et_src = files('et.c')

et_lib = library(
    meson.project_name(),
    include_directories: et_inc,
    sources: et_src,
    install: false,  # TODO(Caleb): Figure out the implications of this.
)

et_dep = declare_dependency(
    include_directories: et_inc,
    link_with: et_lib,
)


# Host dependency
et_host_src = et_src + files('et_host.c')

et_host_lib = library(
    meson.project_name() + '_host',
    include_directories: et_inc,
    sources: et_host_src,
    install: false,  # See above.
)

et_host_dep = declare_dependency(
    include_directories: et_inc,
    link_with: et_host_lib,
)
