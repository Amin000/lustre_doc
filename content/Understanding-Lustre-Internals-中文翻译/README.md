# Understanding Lustre Internals-中文翻译

CTE 4 过线2分的翻译，自己把握哈

对于每个章节的序号，由于把不同的文章都放在一个仓库下，所以章节的序号都会多两级。例如原来的chapter 1的序号为1，放在仓库中，自动生成了1.x.1的章节序号，即如果文章中关于序号的指向为1.2.3，那么在分级目录的序号减去前面两级数字就对应1.2.3。

## 目录

* [Lustre Architecture](./Understanding-Lustre-Internals-中文翻译.md#lustre-architecture)

  * [What is Lustre?](./Understanding-Lustre-Internals-中文翻译.md#what-is-lustre)

  * [Lustre Features](./Understanding-Lustre-Internals-中文翻译.md#lustre-features)

  * [Lustre Components](./Understanding-Lustre-Internals-中文翻译.md#lustre-components)

  * [Lustre File Layouts](./Understanding-Lustre-Internals-中文翻译.md#lustre-file-layouts)

    * [Normal (RAID0) Layouts](./Understanding-Lustre-Internals-中文翻译.md#normal-raid0-layouts)

    * [Composite Layouts](./Understanding-Lustre-Internals-中文翻译.md#composite-layouts)

    * [Distributed Namespace](./Understanding-Lustre-Internals-中文翻译.md#distributed-namespace)

    * [File Identifiers and Layout Attributes](./Understanding-Lustre-Internals-中文翻译.md#file-identifiers-and-layout-attributes)

  * [Lustre Software Stack](./Understanding-Lustre-Internals-中文翻译.md#lustre-software-stack)

* [TEST](./Understanding-Lustre-Internals-中文翻译.md#test)

  * [Lustre Test Suites](./Understanding-Lustre-Internals-中文翻译.md#lustre-test-suites)

  * [Terminology](./Understanding-Lustre-Internals-中文翻译.md#terminology)

  * [Testing Lustre Code](./Understanding-Lustre-Internals-中文翻译.md#testing-lustre-code)

    * [Bypassing Failures](./Understanding-Lustre-Internals-中文翻译.md#bypassing-failures)

    * [Test Framework Options](./Understanding-Lustre-Internals-中文翻译.md#test-framework-options)

  * [Acceptance Small (acc-sm) Testing on Lustre](./Understanding-Lustre-Internals-中文翻译.md#acceptance-small-acc-sm-testing-on-lustre)

  * [Lustre Tests Environment Variables](./Understanding-Lustre-Internals-中文翻译.md#lustre-tests-environment-variables)

* [UTILS](./Understanding-Lustre-Internals-中文翻译.md#utils)

  * [Introduction](./Understanding-Lustre-Internals-中文翻译.md#utils-introduction)

  * [User Utilities](./Understanding-Lustre-Internals-中文翻译.md#user-utilities)

    * [lfs](./Understanding-Lustre-Internals-中文翻译.md#lfs)

    * [lfs _migrate](./Understanding-Lustre-Internals-中文翻译.md#lfs-migrate)

    * [lctl](./Understanding-Lustre-Internals-中文翻译.md#lctl)

    * [llog_reader](./Understanding-Lustre-Internals-中文翻译.md#llogreader)

    * [mkfs.lustre](./Understanding-Lustre-Internals-中文翻译.md#mkfslustre)

  * [mount.lustre](./Understanding-Lustre-Internals-中文翻译.md#mountlustre)

  * [tunefs.lustre](./Understanding-Lustre-Internals-中文翻译.md#tunefslustre)

* [MGC](./Understanding-Lustre-Internals-中文翻译.md#mgc)

  * [Introduction](./Understanding-Lustre-Internals-中文翻译.md#mgc-introduction)

  * [MGC Module Initialization](./Understanding-Lustre-Internals-中文翻译.md#mgc-module-initialization)

  * [MGC obd Operations](./Understanding-Lustre-Internals-中文翻译.md#mgc-obd-operations)

  * [mgc_setup()](./Understanding-Lustre-Internals-中文翻译.md#mgcsetup)

    * [Operation](./Understanding-Lustre-Internals-中文翻译.md#operation)

  * [Lustre Log Handling](./Understanding-Lustre-Internals-中文翻译.md#lustre-log-handling)

    * [Log Processing in MGC](./Understanding-Lustre-Internals-中文翻译.md#log-processing-in-mgc)

  * [mgc_precleanup() and mgc_cleanup()](./Understanding-Lustre-Internals-中文翻译.md#mgcprecleanup-and-mgccleanup)

  * [mgc_import_event()](./Understanding-Lustre-Internals-中文翻译.md#mgcimportevent)

* [OBDCLASS](./Understanding-Lustre-Internals-中文翻译.md#obdclass)

  * [Introduction](./Understanding-Lustre-Internals-中文翻译.md#obdclass-introduction)

  * [obd_device Structure](./Understanding-Lustre-Internals-中文翻译.md#obddevice-structure)

  * [MGC Life Cycle](./Understanding-Lustre-Internals-中文翻译.md#mgc-life-cycle)

  * [Obd Device Life Cycle](./Understanding-Lustre-Internals-中文翻译.md#obd-device-life-cycle)

    * [class_attach()](./Understanding-Lustre-Internals-中文翻译.md#classattach)

    * [obd_export Structure](./Understanding-Lustre-Internals-中文翻译.md#obdexport-structure)

    * [class_setup()](./Understanding-Lustre-Internals-中文翻译.md#classsetup)

    * [class_precleanup() and class_cleanup()](./Understanding-Lustre-Internals-中文翻译.md#classprecleanup-and-classcleanup)

  * [Imports and Exports](./Understanding-Lustre-Internals-中文翻译.md#imports-and-exports)

  * [Useful APIs in Obdclass](./Understanding-Lustre-Internals-中文翻译.md#useful-apis-in-obdclass)

* [LIBCFS](./Understanding-Lustre-Internals-中文翻译.md#libcfs)

  * [Introduction](./Understanding-Lustre-Internals-中文翻译.md#libcfs-introduction)

  * [Data Encryption Support in Libcfs](./Understanding-Lustre-Internals-中文翻译.md#data-encryption-support-in-libcfs)

  * [CPU Partition Table Management](./Understanding-Lustre-Internals-中文翻译.md#cpu-partition-table-management)

  * [Debugging Support and Failure Injection](./Understanding-Lustre-Internals-中文翻译.md#debugging-support-and-failure-injection)

  * [Additional Supporting Software in Libcfs](./Understanding-Lustre-Internals-中文翻译.md#additional-supporting-software-in-libcfs)

* [File Identifiers, FID Location Database, and Object Index](./Understanding-Lustre-Internals-中文翻译.md#file-identifiers-fid-location-database-and-object-index)

  * [File Identifier (FID)](./Understanding-Lustre-Internals-中文翻译.md#file-identifier-fid)

    * [Reserved Sequence Numbers and Object IDs](./Understanding-Lustre-Internals-中文翻译.md#reserved-sequence-numbers-and-object-ids)

    * [fid Kernel Module](./Understanding-Lustre-Internals-中文翻译.md#fid-kernel-module)

  * [FID Location Database (FLD)](./Understanding-Lustre-Internals-中文翻译.md#fid-location-database-fld)

  * [Object Index (OI)](./Understanding-Lustre-Internals-中文翻译.md#object-index-oi)
