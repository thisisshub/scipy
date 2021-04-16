include_dirs = run_command(python,
    ['-c', 'import pybind11; include_dirs = [pybind11.get_include(True), pybind11.get_include(False)]'], 
    check : true).stdout().strip()

gen_src =  custom_target(
    'pypocketfft',
    includedir : include_dirs,
    output : 'pocketfft_hdronly.h',
    input : 'pypocketfft.cxx',
    command : [python, '@INPUT@', '--header', '@OUTPUT@', '--incdir=@INCLUDEDIR@']   
)

run_command(python, 'import scipy._pocketfft as mod; mod.test()')