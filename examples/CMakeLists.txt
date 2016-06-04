set( examples
    demo1
)

foreach( example ${examples} )
    add_executable( ${example} ${example}.c )
    set_source_files_properties( ${example}.c PROPERTIES LANGUAGE C )
    target_link_libraries( ${example} ${OpenBLAS_LIBNAME} )
endforeach( example )
