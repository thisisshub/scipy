project(
    'scipy',
    version: '1.6.2',
    license: 'BSD',
    meson_version: '>=0.55',
)

python = find_program('python3')

# Ensure python is installed and found
if not python.found()
    error('No python binary found')
endif

subdir('scipy/constants')
subdir('scipy/fft')