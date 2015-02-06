add_library(boost_numpy STATIC
  # header files
  ../../../boost/numpy/dtype.hpp
  ../../../boost/numpy/internal.hpp
  ../../../boost/numpy/invoke_matching.hpp
  ../../../boost/numpy/matrix.hpp
  ../../../boost/numpy/ndarray.hpp
  ../../../boost/numpy/numpy_object_mgr_traits.hpp
  ../../../boost/numpy/scalars.hpp
  ../../../boost/numpy/ufunc.hpp

  # source files (in current directory)
  dtype.cpp
  scalars.cpp
  ndarray.cpp
  matrix.cpp
  ufunc.cpp
  numpy.cpp
)

target_link_libraries(boost_numpy ${BOOST_LIBRARYDIR}/libboost_python.a ${PYTHON_LIBRARIES})
