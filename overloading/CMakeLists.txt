add_executable(proc pragma.f90)
add_test(NAME FortranPragma COMMAND proc)

if(f18errorstop)
  add_executable(f18es f2018errorstop.f90)
  add_test(NAME F18errorstop COMMAND f18es)
  set_tests_properties(F18errorstop PROPERTIES WILL_FAIL true)
endif()
