# pimple-viv-error
https://cfd-china.com/topic/4394/%E7%94%A8pimplefoam%E5%81%9A%E5%9C%86%E6%9F%B1%E7%9A%84%E6%B6%A1%E6%BF%80%E6%8C%AF%E5%8A%A8%E9%81%87%E5%88%B0%E6%94%B6%E6%95%9B%E6%80%A7%E9%97%AE%E9%A2%98

```bash
PIMPLE: Iteration 1
Restraint verticalSpring:  attachmentPt - anchor (0 1.14264e-05 0) spring length 1.14264e-05 force (-0 -4.72392e-05 -0)
6-DoF rigid body motion
    Centre of rotation: (0 1.14788e-05 0.084)
    Centre of mass: (0 1.14788e-05 0.084)
    Orientation: (1 0 0 0 1 0 0 0 1)
    Linear velocity: (0 2.61184e-05 0)
    Angular velocity: (0 0 0)
GAMG:  Solving for pcorr, Initial residual = 1, Final residual = 0.0197574, No Iterations 40
GAMG:  Solving for pcorr, Initial residual = 0.27233, Final residual = 0.0156253, No Iterations 4
time step continuity errors : sum local = 3.08875e-14, global = 7.0696e-15, cumulative = 9.56635e-09
smoothSolver:  Solving for Ux, Initial residual = 3.30404e-06, Final residual = 3.30404e-06, No Iterations 0
smoothSolver:  Solving for Uy, Initial residual = 0.000208158, Final residual = 1.22015e-07, No Iterations 1
smoothSolver:  Solving for Uz, Initial residual = 2.49119e-05, Final residual = 1.94723e-08, No Iterations 1
GAMG:  Solving for p, Initial residual = 0.212445, Final residual = 0.00136547, No Iterations 4
GAMG:  Solving for p, Initial residual = 0.0257973, Final residual = 9.60752e-07, No Iterations 45
time step continuity errors : sum local = 1.04039e-13, global = -1.47872e-14, cumulative = 9.56634e-09
PIMPLE: Iteration 2
smoothSolver:  Solving for Ux, Initial residual = 1.52276e-06, Final residual = 1.52276e-06, No Iterations 0
smoothSolver:  Solving for Uy, Initial residual = 9.39697e-05, Final residual = 1.19676e-07, No Iterations 1
smoothSolver:  Solving for Uz, Initial residual = 1.10536e-05, Final residual = 2.00238e-08, No Iterations 1
GAMG:  Solving for p, Initial residual = 0.25598, Final residual = 0.00164346, No Iterations 4
[0] #0  Foam::error::printStack(Foam::Ostream&) at ??:?
[0] #1  Foam::sigSegv::sigHandler(int) at ??:?
[0] #2  ? in "/lib/x86_64-linux-gnu/libc.so.6"
[0] #3  Foam::lduMatrix::Amul(Foam::Field<double>&, Foam::tmp<Foam::Field<double> > const&, Foam::FieldField<Foam::Field, double> const&, Foam::UPtrList<Foam::lduInterfaceField const> const&, unsigned char) const at ??:?
[0] #4  Foam::GAMGSolver::scale(Foam::Field<double>&, Foam::Field<double>&, Foam::lduMatrix const&, Foam::FieldField<Foam::Field, double> const&, Foam::UPtrList<Foam::lduInterfaceField const> const&, Foam::Field<double> const&, unsigned char) const at ??:?
[0] #5  Foam::GAMGSolver::Vcycle(Foam::PtrList<Foam::lduMatrix::smoother> const&, Foam::Field<double>&, Foam::Field<double> const&, Foam::Field<double>&, Foam::Field<double>&, Foam::Field<double>&, Foam::Field<double>&, Foam::Field<double>&, Foam::PtrList<Foam::Field<double> >&, Foam::PtrList<Foam::Field<double> >&, unsigned char) const at ??:?
[0] #6  Foam::GAMGSolver::solve(Foam::Field<double>&, Foam::Field<double> const&, unsigned char) const at ??:?
[0] #7  Foam::fvMatrix<double>::solveSegregated(Foam::dictionary const&) at ??:?
[0] #8  Foam::fvMatrix<double>::solve(Foam::dictionary const&) in "/home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/bin/pimpleFoam"
[0] #9  Foam::fvMatrix<double>::solve() in "/home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/bin/pimpleFoam"
[0] #10  ? in "/home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/bin/pimpleFoam"
[0] #11  __libc_start_main in "/lib/x86_64-linux-gnu/libc.so.6"
[0] #12  ? in "/home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/bin/pimpleFoam"
[111:1838841] *** Process received signal ***
[111:1838841] Signal: Segmentation fault (11)
[111:1838841] Signal code:  (-6)
[111:1838841] Failing at address: 0x3e8001c0ef9
[111:1838841] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x46210)[0x7f5a7570c210]
[111:1838841] [ 1] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0xcb)[0x7f5a7570c18b]
[111:1838841] [ 2] /lib/x86_64-linux-gnu/libc.so.6(+0x46210)[0x7f5a7570c210]
[111:1838841] [ 3] /home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/lib/libOpenFOAM.so(_ZNK4Foam9lduMatrix4AmulERNS_5FieldIdEERKNS_3tmpIS2_EERKNS_10FieldFieldIS1_dEERKNS_8UPtrListIKNS_17lduInterfaceFieldEEEh+0x1dc)[0x7f5a76140c3c]
[111:1838841] [ 4] /home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/lib/libOpenFOAM.so(_ZNK4Foam10GAMGSolver5scaleERNS_5FieldIdEES3_RKNS_9lduMatrixERKNS_10FieldFieldIS1_dEERKNS_8UPtrListIKNS_17lduInterfaceFieldEEERKS2_h+0x62)[0x7f5a76166dc2]
[111:1838841] [ 5] /home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/lib/libOpenFOAM.so(_ZNK4Foam10GAMGSolver6VcycleERKNS_7PtrListINS_9lduMatrix8smootherEEERNS_5FieldIdEERKS8_S9_S9_S9_S9_S9_RNS1_IS8_EESD_h+0x885)[0x7f5a7616ae35]
[111:1838841] [ 6] /home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/lib/libOpenFOAM.so(_ZNK4Foam10GAMGSolver5solveERNS_5FieldIdEERKS2_h+0x524)[0x7f5a7616d154]
[111:1838841] [ 7] /home/abc/OpenFOAM/OpenFOAM-8/platforms/linux64GccDPInt32Opt/lib/libfiniteVolume.so(_ZN4Foam8fvMatrixIdE15solveSegregatedERKNS_10dictionaryE+0x18b)[0x7f5a783322ab]
[111:1838841] [ 8] pimpleFoam(_ZN4Foam8fvMatrixIdE5solveERKNS_10dictionaryE+0x1e8)[0x55f9e9e962e8]
[111:1838841] [ 9] pimpleFoam(_ZN4Foam8fvMatrixIdE5solveEv+0x120)[0x55f9e9e96590]
[111:1838841] [10] pimpleFoam(+0x2e50b)[0x55f9e9e4450b]
[111:1838841] [11] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0xf3)[0x7f5a756ed0b3]
[111:1838841] [12] pimpleFoam(+0x313fe)[0x55f9e9e473fe]
[111:1838841] *** End of error message ***
--------------------------------------------------------------------------
Primary job  terminated normally, but 1 process returned
a non-zero exit code. Per user-direction, the job has been aborted.
```
