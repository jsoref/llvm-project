add_mlir_dialect_library(MLIRAffineOps
  AffineOps.cpp
  AffineValueMap.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/Affine

  DEPENDS
  MLIRAffineOpsIncGen
  )
target_link_libraries(MLIRAffineOps
  PUBLIC
  MLIREDSC
  MLIRIR
  MLIRLoopLikeInterface
  MLIRSideEffects
  MLIRStandardOps
  )
