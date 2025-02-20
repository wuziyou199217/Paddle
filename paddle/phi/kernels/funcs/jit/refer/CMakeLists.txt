cc_library(
  jit_kernel_refer
  SRCS refer.cc
  DEPS jit_kernel_base)
set(JIT_KERNEL_DEPS
    ${JIT_KERNEL_DEPS} jit_kernel_refer
    PARENT_SCOPE)

function(USE_JITKERNEL_REFER TARGET)
  file(APPEND ${jit_file} "USE_JITKERNEL_REFER(${TARGET});\n")
endfunction()

# use refer kernel by name
use_jitkernel_refer(kVMul)
use_jitkernel_refer(kVAdd)
use_jitkernel_refer(kVAddRelu)
use_jitkernel_refer(kVSub)
use_jitkernel_refer(kVScal)
use_jitkernel_refer(kVAddBias)
use_jitkernel_refer(kVCopy)
use_jitkernel_refer(kVRelu)
use_jitkernel_refer(kVIdentity)
use_jitkernel_refer(kVExp)
use_jitkernel_refer(kVSigmoid)
use_jitkernel_refer(kVTanh)
use_jitkernel_refer(kLSTMCtHt)
use_jitkernel_refer(kLSTMC1H1)
use_jitkernel_refer(kGRUH1)
use_jitkernel_refer(kGRUHtPart1)
use_jitkernel_refer(kGRUHtPart2)
use_jitkernel_refer(kCRFDecoding)
use_jitkernel_refer(kLayerNorm)
use_jitkernel_refer(kSeqPool)
use_jitkernel_refer(kMatMul)
use_jitkernel_refer(kVSquare)
use_jitkernel_refer(kEmbSeqPool)
use_jitkernel_refer(kAdam)
use_jitkernel_refer(kAdamW)
use_jitkernel_refer(kSgd)
use_jitkernel_refer(kVBroadcast)
