project(
    'scipy',
    version: '1.6.2',
    license: 'BSD',
    meson_version: '>=0.55',
)

pymod = find_program('python3')

# Tests
run_command(pymod, 'import scipy.constants as mod; mod.test()')