# Lustre doc

* [介绍](README.md)

* [Understanding Lustre Internals 中文翻译](content/Understanding-Lustre-Internals-中文翻译/README.md)
  * [Lustre Architecture](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-architecture)

    * [What is Lustre?](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#what-is-lustre)

    * [Lustre Features](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-features)

    * [Lustre Components](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-components)

    * [Lustre File Layouts](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-file-layouts)

      * [Normal (RAID0) Layouts](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#normal-raid0-layouts)

      * [Composite Layouts](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#composite-layouts)

      * [Distributed Namespace](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#distributed-namespace)

      * [File Identifiers and Layout Attributes](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#file-identifiers-and-layout-attributes)

    * [Lustre Software Stack](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-software-stack)

  * [TEST](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#test)

    * [Lustre Test Suites](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-test-suites)

    * [Terminology](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#terminology)

    * [Testing Lustre Code](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#testing-lustre-code)

      * [Bypassing Failures](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#bypassing-failures)

      * [Test Framework Options](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#test-framework-options)

    * [Acceptance Small (acc-sm) Testing on Lustre](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#acceptance-small-acc-sm-testing-on-lustre)

    * [Lustre Tests Environment Variables](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-tests-environment-variables)

  * [UTILS](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#utils)

    * [Introduction](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#utils-introduction)

    * [User Utilities](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#user-utilities)

      * [lfs](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lfs)

      * [lfs _migrate](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lfs-migrate)

      * [lctl](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lctl)

      * [llog_reader](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#llogreader)

      * [mkfs.lustre](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mkfslustre)

    * [mount.lustre](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mountlustre)

    * [tunefs.lustre](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#tunefslustre)

  * [MGC](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgc)

    * [Introduction](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgc-introduction)

    * [MGC Module Initialization](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgc-module-initialization)

    * [MGC obd Operations](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgc-obd-operations)

    * [mgc_setup()](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgcsetup)

      * [Operation](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#operation)

    * [Lustre Log Handling](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#lustre-log-handling)

      * [Log Processing in MGC](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#log-processing-in-mgc)

    * [mgc_precleanup() and mgc_cleanup()](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgcprecleanup-and-mgccleanup)

    * [mgc_import_event()](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgcimportevent)

  * [OBDCLASS](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#obdclass)

    * [Introduction](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#obdclass-introduction)

    * [obd_device Structure](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#obddevice-structure)

    * [MGC Life Cycle](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#mgc-life-cycle)

    * [Obd Device Life Cycle](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#obd-device-life-cycle)

      * [class_attach()](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#classattach)

      * [obd_export Structure](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#obdexport-structure)

      * [class_setup()](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#classsetup)

      * [class_precleanup() and class_cleanup()](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#classprecleanup-and-classcleanup)

    * [Imports and Exports](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#imports-and-exports)

    * [Useful APIs in Obdclass](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#useful-apis-in-obdclass)

  * [LIBCFS](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#libcfs)

    * [Introduction](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#libcfs-introduction)

    * [Data Encryption Support in Libcfs](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#data-encryption-support-in-libcfs)

    * [CPU Partition Table Management](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#cpu-partition-table-management)

    * [Debugging Support and Failure Injection](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#debugging-support-and-failure-injection)

    * [Additional Supporting Software in Libcfs](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#additional-supporting-software-in-libcfs)

  * [File Identifiers, FID Location Database, and Object Index](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#file-identifiers-fid-location-database-and-object-index)

    * [File Identifier (FID)](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#file-identifier-fid)

      * [Reserved Sequence Numbers and Object IDs](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#reserved-sequence-numbers-and-object-ids)

      * [fid Kernel Module](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#fid-kernel-module)

    * [FID Location Database (FLD)](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#fid-location-database-fld)

    * [Object Index (OI)](content/Understanding-Lustre-Internals-中文翻译/Understanding-Lustre-Internals-中文翻译.md#object-index-oi)
