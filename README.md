[![Discord](https://img.shields.io/discord/423767742546575361.svg?label=&logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)](https://discord.gg/vpEv3HJ)
<a href=" https://github.com/moshix/mvs/blob/master/codenotary.com"><img src="https://raw.githubusercontent.com/moshix/mvs/master/secured-by-immudb.svg" width="109px;"/></a>
<a href="https://cas.codenotary.com"><img src="https://raw.githubusercontent.com/codenotary/cas/master/extra/badge/secured-by-cas.svg" width="119px;"/></a>
<h1> Most Common MVS ABEND Codes</h1>


<pre>
S001-01 An I/O error occurred during BDAM create, BSAM, BISAM, QSAM, or BDAM and no SYNAD exit was specified by the user.
S001-02 An error was encountered while attempting to close the dataset.
S001-03 For QSAM, an error was encountered that could not be accepted.
S001-04 For QSAM, ABE or an invalid value for EROPT parameter in the DCB and/or no error handling (SYNAD) exit was specified.
S001-05 For QSAM, a GET was issued after end-of-file.
S002 DCB had the wrong block size, IEHMOVE-attempt to rename dataset when new name already exists, wrong RECORD format specified in JCL.
S002-04 An invalid record was encountered on a GET operation. The length field of a record descriptor word (RDW) for a variable length record specifies a value less than 4.
S002-08 An invalid record was encountered on a PUT or WRITE operation. The record or block length plus the key length and required overhead is greater than the DASD track capacity.
S002-10 An invalid record was encountered on a PUT or WRITE operation. The dataset uses the track overflow feature. The RDW for a variable length record specifies a length greater than 32,752.
S002-14 An invalid record was encountered on a PUT or WRITE operation. The record length is greater than the blocksize specified in the DCB.
S002-18 An invalid record was encountered on a PUT operation; the dataset uses the variable record format. The length value of the RDW is either: less than 4, greater than 32,767, greater than the blocksize specified in the DCB, or less than 5 if ASA control characters are being used.
S002-1C The error was issued for a record larger than the track capacity, and the record format does not use the track overflow feature.
S002-20 The error occurred during the creation of a direct dataset. A write macro was issued causing a secondary extent to be obtained. The block will not fit on the amount of space allocated for the secondary extent.
S002-24 The error occurred during the creation of a direct dataset. A write macro was issued to write out a block larger than the primary extent on the preallocated dataset. This could also occur if allocation of the primary extent as non-contiguous and any of the secondary extents were smaller than the block.
S002-28 The error occurred during the creation of a direct dataset. During the execution of open it was detected that the blocksize was larger than the primary extent.
S002-2C The error occurred while opening an ISAM dataset. Too many tracks were specified for cylinder overflow.
S013 Conflicting or incomplete parameters in DCB, such as BLKSIZE not a multiple of LRECL, or missing SYSIN DD; Tried to create a PDS without allocating directory blocks; Member name specified in DD not found; no directory allocation subparameter in DD; Open output dataset as input; Track overflow or updating attempted, but not supported by the OS. May be a record length or OPEN statement error.
S013-08 ANSI standard labels were specified in the LABEL parameter but are not supported by the system.
S013-0C A buffer length of 0 was specified for a BDAM dataset for which dynamic buffering was requested.
S013-10 An OPEN macro was issued for a null dataset and blocksize and BUFL are both 0. Specify one or the other as non-zero.
S013-14 An OPEN macro was issued with output or outin specified. DCB specifies DSORG=PO, but the DSCB indicates the dataset is not partitioned. Change DSORG to PS, or create dataset as PDS.
S013-18 An open was issued for a partitioned dataset. The specified member name was not found in the dataset.
S013-1C An OPEN macro was issued for a partitioned dataset, but an I/O error was encountered searching the directory.
S013-20 An OPEN macro was issued for a sequential dataset using the queued access technique with RECFM=FB, but blocksize is not a multiple of LRECL, or for variable-length records, blocksize is not 4 bytes greater than the LRECL.
S013-24 An open was issued with input, inout, RDBACK, or updat specified, but the DCB MACRF did not specify EXCP, GET, or READ.
S013-28 An OPEN macro was issued with output or outin specified, but the DCB MACRF did not specify EXCP, PUT, or WRITE.
S013-2C A sequential dataset using the queued access technique with exchange buffering was opened for input, but the buffer control block address was 0.
S013-30 A sequential dataset using the queued access technique with exchange buffering was opened for output, but the buffer control block address was 0.
S013-34 An OPEN macro was issued for a dataset with blocksize and BUFL equal to 0. The system determined that it had to obtain buffers but was unable to do so
S013-38 An OPEN macro was issued for a sequential dataset on a direct access device with track overflow, but the buffer control block address was zero.
S013-3C A sequential dataset was opened for input or output, but the buffer control block address was 0. This type of error often occurs is a DCB is shared by two or more tasks, or is opened and closed several times within one job step.
S013-40 A sequential or direct dataset was opened for input, but the buffer control block address was 0.
S013-44 An OPEN macro was issued for a dataset on a direct access device for which chained scheduling was specified, but the buffer control block address was 0.
S013-48 An OPEN macro was issued for a sequential dataset using the queued access technique, but the buffer control block address was zero.
S013-4C An OPEN macro was issued for a sequential dataset using the queued access technique. The system determined that a buffer pool existed for this dataset and made the appropriate test shown below with unsatisfactory results: If the data was to be sent directly to a unit record device (no spooling), the buffer length value in the buffer control block had to be equal or greater than the value specified in the DCB for logical record length. Otherwise the buffer length in the buffer control block had to be equal or greater than the value specified in the DCB for BLKSIZE.
S013-50 An OPEN macro issued for a dataset allocated to a printer did not have output specified as an open option.
S013-58 An OPEN macro was issued for a paper tape dataset and concatonation with unlike attributes was specified.
S013-5C An OPEN macro was issued for a sequential dataset using the queued access technique. The dataset contained spanned variable length records larger than 32,756 but GET locate mode was not used.
S013-60 An OPEN macro was issued for a dataset with a DCB specifying RECFM=F, and blocksize was not equal to LRECL. Correct the RECFM to FB, or make LRECL and blocksize equal.
S013-64 An OPEN macro was issued for a null dataset using an access method other than QSAM or BSAM. This is a no-no.
S013-68 An OPEN macro was issued for a dataset whose DCB specified a BLKSIZE greater than 32,767, which is the maximum allowed.
S013-70 An OPEN macro was issued for a dataset on magnetic tape. A conflict exists among LABEL parameters on the DD statement and DCBRECFM, DCBOPTCD, DCBBUFOF and DCBUSASI give the appearance of mixed USASI and EBCDIC attributes to the dataset; or OPTCD=q was specified for a dataset on a devise other than magnetic tape.
S013-74 An OPEN macro was issued for an optical character reader dataset, but the open option did not specify INPUT.
S013-78 An OPEN macro was issued for an optical character reader dataset, but the BUFL parameter was specified as 0.
S013-7C An OPEN macro was issued for an optical character reader dataset, but the BUFL parameter in the DCB was specified as 0.
S013-80 An OPEN macro was issued for an optical character reader dataset, but the LRECL parameter was less than the BUFL.
S013-84 An OPEN macro was issued for an optical character reader dataset. The number of buffers specified in the buffer pool control block is not the same as that specified in the DCBBUFNO.
S013-88 An OPEN macro was issued for a telecommunications device but the DCBDSORG did not specify so.
S013-8C An OPEN macro was issued for a direct organization dataset (BDAM) but the DCBRECFM parameter was not specific.
S013-A4 A DCB was opened for a SYSIN or SYSOUT dataset but the DSORG was not specified as PS.
S013-A8 An invalid record format was requested for a SYSIN or SYSOUT dataset. (RECFM=D, vs, or VBS are Invalid for SYSIN)
S013-B0 An OPEN macro was issued with the Reback option for a DCB specifying a record format of variable spanned records. These are conflicting parameters.
S013-B4 An OPEN macro was issued with the INOUT/OUTIN option for a DCB specifying the QSAM MACRF values; these are conflicting parameters.
S013-BC A SYSIN or SYSOUT DCB was opened with invalid options. Either open specified UPDAT or RDBACK, or the point macro function was specified in MACRF=RP or WP. Repositioning or updating a spooled dataset is not permitted.
S013-C0 A SYSIN or SYSOUT Dataset could not be opened by a job entry subsystem. The failing DCB is not opened, however the task is not terminated. Processing continues for other DCBS opened.
S013-C4 During the creation of a direct dataset, the open routine found that the DCB specified READ (R) or GET (G) in the MACRG field. Only WRITE LOAD (WL) is allowed.
S013-C8 The open subsystem executor module was passed an error return code in register 15 after issuing the IEFSSREQ macro to connect the user's ACB to the subsystem. This indicates the subsystem was not operating.
S028 A paging operation has not completed successfully due to one of the following: -A permanent I/O error occurred while attempting a page-in or swap-in operation. The data being paged in or swapped in is lost.  -A real storage management routine or another system routine performing a service for RSM suffered an intermediate error. The function performed is terminated.  -An auxiliary storage management routine suffered a translation error while using the control register of another address space to update that address space's LSQA.
SO3B ISAM dataset to be processed, but not created or its DCB not closed after creation. - Possible cause: dataset was to be written on but was opened as input. LRECL/BLKSIZE problem exists-invalid values or not multiples.
SO3D The error occurred during the execution of a QISAM or BISAM or BDAM macro instructions.
S03D-04 An OPEN macro was issued for an indexed sequential or direct dataset. The volume serial numbers on the DD statement were not specified in the same order that the dataset was created.
S03D-08 An OPEN macro was issued for an indexed sequential dataset. The first volume of the dataset does not have a format2 DSCB.
S03D-0C An OPEN macro was issued for a direct dataset. The dataset has an indexed sequential organization.
S047 An unauthorized program requested a restricted SVC.
S071 The operator pressed the restart key to activate the system's recovery and termination process. The program running at the time the operator pressed the restart button was sent through abend processing because the operator determined it was a noncancelable loop or wait state.
S07C Supervisor control recovery has detected an error which requires that the current task be terminated or that the current address space be terminated.
S0B0 An uncorrectable error was detected by the SWA Manager.
S0B0-04 Invalid function requested.
S0B0-08 Invalid SVA (Does not point to the beginning of a SWA prefix or the SWA prefix has been destroyed.
S0B0-10 Invalid length (0 or negative for asign locate or attempting to read or write a record which is not 176 bytes, in move mode).
S0B0-14 Invalid coutn field (0 for read, write assign or 00 for write and assign).
S0B0-18 QMNGRIO macro was issued with both or neither of the read and write bits set.
S0B0-1C Invalid ID. (The caller attempted to write a block for the first time and has either passed an non-existing ID or has failed to pass one and the block does not have an embedded ID.
S0B0-20 Invalid block pointer (write locate is attempting to write and is passing a block pointer which is not valied for the SVA requested).
S0C1 Operation Exception - An Operation is code is not on the machine. Possible Causes: subscript error - clobbered code tried to read a file that was not open misspelled DDName error in parameters passed to subroutines missing DD card RECORDING MODE i wrong or density is incorrect bad load module, possible bad object deck FORTRAN - Missing DIMENSION statement, same name for array and subroutine COBOL - subroutine PROGRAM ID is the same as the ENTRY name.  COBOL - tried to CALL within COBOL F SORT INPUT/OUTPUT PROCEDURE COBOL - tried to CALL a subroutine which could not be found COBOL - incomplete DCB for SORTIN COBOL - using SORT verb, DDNAME was not SORTOUT when GIVING option used.  COBOL - executing sort-using after opening SORTIN
S0C2 Privileged operation exception. Unintentional branch to invalid instruction due to subscript error. COBOL -missing period at end of paragraph or paragraph names missing GOBACK after sort verb. Logic fell into input procedure. ACCEPT verb was executed when no SYSIN DD was available.
S0C3 Failure to close input/output file in source code.
S0C4 Protection exception - virtual address could not be translated into a real address; Possible subscript error or bad parms; Variable length record larger than maximum target field size; missing or misspelled dd statement; I/O against unopened file; Using GOBACK in an output procedure; Move to an area not passed in a CALL statement; COBOL Sort with STOP RUN in input or output procedure; blocksize and logical record size equal for a variable length dataset.
S0C5 Index or subscript out of range; uninitialized index or subscript; invalid data address; Reference to a field in a record before OPEN or after CLOSE; Closing the same file twice; improper exit of a PERFORM statement; 88 level cannot be last statement before Report section; date not initialized; Problem with a GO TO, GO TO DEPENDING ON, or GO TO that has been ALTERED.
S0C6 Specifcation exception -an incorrect boundary was specified. Usually caused by unintentional branch to invalid instruction. Ddname/Select statement conflict; ACCEPT statement with SYSIN DD and data missing; No GO TO statement in a paragraph named in an ALTER statement; I/O attempted against a file not open.
S0C7 Data exception -decimal data is incorrect or improperly overlapped or not validly initialized. Subscript error, referenced beyond table. COBOL -working storage not initialized. -bad data, should check data for errors. -Garbage in a filed being tested; subroutine parm missing or in wrong order.
S0C8 Fixed point overflow exception note -masked by FORTRAN.
S0C9 Fixed point divide exception note-masked by FORTRAN.
S0CA Decimal overflow exception. The destination field is too small to contain the result field in a decimal operation.
S0CB Decimal divide exception. A quotient exceeds the specified data field size.
S0CC Exponent overflow exception. A floating point number exceeds the maximum size. Note- This error is detected and fixed in FORTRAN.
S0CD Exponent underflow exception. A floating point number is smaller than the minimum. Note -FORTRAN will set the result to zero and continue processing.
S0CE Significance exception a floating point addition or subtraction results in an all zero fraction note -this is masked in FORTRAN.
S0CF Floating point divide exception -divide by zero note- this error is detected and noted by FORTRAN.
S0D2 A program check was detected; an interruption code of 18 (translation specification exception) has occurred. There is invalid data in either control registers 0 or 1, or a segment or page table. The error is the result of a hardware error or a program running in key zero has caused data damage.
S0D3 A program check was detected; and interruption code of 19 (special operation error) has occurred. A privileged program issued a set system mask. This instruction is not valid in OS/VS2 (since Release 2).
SOE3 The error occurred while processing a VIO dataset. The system was unable to assign, locate, fix, free, or access VIO pages for the dataset. Please report this problem to the systems group.
SOF1 Program interruption in I/O interruption handler record described as wrong length.
SOF2 Program interruption in Type 1 SVC routine clobbered IOB or other SVC paramters -see SOC1.
SOF3 Machine check interruption disk I/O failure or machine trouble.
SOF8 The issuer of an SVC was either in SRB mode, held a lock, or was disabled.
S100 A device to be used was not operational or a pseudo device previously allocated has been reallocated.
S102 The error occurred during execution of a post macro instruction. The control program found an invalid event control block address, or the ECB was in a storage area with a protection key different from that of the task issuing the macro.
S106 Region size too small. An error was detected by the control program when it attempted to fetch the requested program into virtual storage. Possible cause: Previous LKED step failed to output a SYSLMOD, needs larger SIZE=I/O error-machine trouble or disk failure.
S106-0B A program check or loop occurred in fetch.
S106-0C Not enough storage was available for fetch to do a GETMAIN for the module or control blocks.
S106-0D The control program found an invalid record type in the load module
S106-0E The control program found an invalid address in the load module
S106-0F An uncorrectable input/output error occurred.
S122 Either the operator or the job entry subsystem cancelled the job, requesting a dump. Check the job log listing for more information.
S12D Invalid segment table in an overlay program. See S0C1.
S130 The DEQ macro specified a resource not previously specified by an ENQ macro. That is, the program had not requested control of a resource it was attempting to release.
S137 I/O error in end of volume label processing on magnetic tape.
S137-04 An I/O error occurred while writing an end of volume label or tape mark.
S137-08 An I/O error occurred while positioning the tape in preparation for label processing.
S137-0C An I/O error occurred reading a trailer label for a dataset opened with the input or inout option, or reading the header label for a dataset opened with the RDBACK option.
S137-10 An I/O error occurred while positioning a magnetic tape at the end of the dataset.
S137-14 An I/O error occurred reading header labels for a dataset opened for input or inout, or reading the trailer label for a dataset opened for RDBACK.
S137-18 An I/O error occurred while positioning a magnetic tape dataset at the first data record.
S137-1C An invalid trailer label was read during end of volume.
S137-20 An invalid header label was read during end of volume.
S137-24 A specific volume serial number was specified for the second or subsequent volume of an output dataset on magnetic tape. During EOV processing, it was discovered that the expiration date (from the HDR1 label of the first dataset currently on the specified volume) had not passed. When requested to specify whether the volume could be used in spit of the expiration date, the operator did not reply 'U'. Ask the operator to reply 'U' or specify another volume serial.
S138 The error occurred during the execution of an ENQ macro. Two ENQ macros were issued for the same resource in the same task without an intervening DEQ macro. The second ENQ macro did not specify test, use, or have in its RET operand.
S13E The task which created a subtask has issued a detach for that subtask, specifying STAE=NO, before that subtask has terminated.
S14F The routine attempted to execute the STATUS macro instruction for other than the STOP, STOP SYNCH, OR START function and was not in supervisor key(0-7).
S16E The control program requested that a DEBCHK function be performed on a data extent block obtained from the DCB passed by the program. That function could not be completed.
S16E-04 The indicated DEB pointer is not in the DEB table. A DEB whose address is not in the DEB table cannot be verified, deleted, or purged.
S16E-08 Invalid type specified (macro not issued). Acceptable types are ADD, DELETE, VERIFY, and PURGE.
S16E-10 DEBDCBAD does not point to DCB. It is normally assumed that the DCBDEBAD field of the DCB points to the DEB, but the DEBDCABAD field of the DEB must point to the DCB when TYPE=VERIFY, ADD, or DELETE.
S16E-14 AM value does not equal DEBAMTYP value. When a DEB pointer is added to the table, the access method pointer (AM) value, if given is placed in the DEBAMTYP field of the DEB. If no AM value is coded, A O is inserted in the field, subsequent DEBCHKS issued to verify or delete that DEB pointer must either specify the same AM value or omit the operand. When the operand is omitted, no comparison is made.
S16E-18 DEB not on the TCB chain for type=ADD. Before the DEB pointer can be added to the table, the DEB itself must be queued on the current TCB DEB chain.
S16E-1C DEBAMTYP or DEBTBLOF=0 for TYPE=ADD. Values other than 0 indicate a pointer to this DEB already exists in the DEB table.
S16E-20 DEB table contains 32760 bytes and TYPE=ADD. The current DEB table does not have space for this new DEB pointer. To increase the table size by the required increment of 24 would cause the table to exceed its maximum size.
S171 The real storage manager was invoked with a request for a PGFIX, PGFREE, PGLOAD or PGOUT service and the request was illegal or invalid. The request is considered to be illegal if the storage range specified by the input parameters does not exist (a GETMAIN was not issued for it). NOTE: The meanings of the contents of general registers 11, 12, 13 and 14 are provided for diagnostic purposes in the full description of this abend in the SYSTEM CODES MANUAL. Possible causes: input parameter error in virtual subarea list (VSL) VSL not on a fullword boundary VSL NOT IN FIXED STORAGE undefined or conflicting option flags. End address of range not greater than beginning address.  an option was specified which is not supported by MVS. These are RSAOPT and ECBIND.  VSL is store protected from the caller ECB not on fullword boundary ECB is store-protected from caller ECB not specified for PGFIX.  ECB specified for PGOUT
S171-04 The error was detected by the page services routine. This generally indicates that the caller did not own the virtual storage defined by the VSL list entry.
S171-16 The input VSL or ECB failed to pass the page services interface validity check.
S206 The address of the parameter list, or one of the parameters passed to a LINK, LOAD, XCTL, or DELETE macro invalid.
S213 DSCB not found; I/O error in reading or writing DSCB. Possible causes: the data set is not the specified volume DISP=MOD is not compatible with a volume reference incorrect tape positioning.
S213-04 An I/O error occurred reading the FORMAT 1 DSCB, or the FORMAT 1 DSCB could not be found on the first volume specified by the DD statement volume serial field.
S213-08 An OPEN macro was issued for a password protected dataset but the system was unable to locate the password dataset.
S213-0C An I/O error occurred reading a FORMAT 1 DSCB for a direct or indexed sequential dataset, or the FORMAT 1 DSCB could not be found on the volume specified by the DD statement.
S213-18 An I/O error occurred writing back a FORMAT 1 DSCB.
S213-20 During an open, a volume contained more than 16 extends of the indicated dataset. Try browsing or editing the file via SPF 3.4. Check the upper right-most corner of the ISPF panel for an indicator message.
S213-28 An OPEN macro ws issued for a direct access dataset specifying UNIT=SYSDA, but the UNIT already contained 127 users, whcih is the maximum allowed.
S214 I/O error in tape positioning or volume disposition.
S214-04 An I/O error occurred reading a user label on magnetic tape.
S214-08 An I/O error positioning a magnetic tape volume during execution of a CLOSE macro.
S222 Either the operator or the job enter subsystem cancelled the job. Check the job log listing for more information. If there is no apparent explanation, contact operations before resubmitting. Possible causes: Line or card estimate exceeded.  JCL error caused mount request Excessive runtime.
S233 Invalid parameters have been passed to SVC dump.
S233-04 The address of the parameter list is zero.
S233-08 The parameter list is not a valid SVC dump or snap parameter list for MVS.
S233-0C The caller-supplied dataset is on an unsupported device.
S233-10 In a user-supplied storage range, the start address is greater than the end address.
S233-14 The user-supplied data (for HDR= or HDRAD=) is greater than 100 characters.
S233-18 The 4K SQA buffer has been requested (BUFFER=YES) but it is not serialized (by setting on the high order bit in CVTSDBF)
S233-1C The parameter list or what it points to is in the 4K SQA buffer.
S233-20 The user supplied a DCB address and the DCB is not open, or the DCB address is invalid.
S233-24 The specified ASID parameter was syntactically invalid. The ASID was less than 0 or greater than the maximum value.
S233-28 An ASID specified in the ASID list pointed to the by the ASIDLST parameter was syntactically invalid. The ASID was less than 0 or greater than the maximum value.
S233-2C The ASIDLST address is zero, or points to an area that the user cannot reference.
S233-38 The caller specifoed the 4K SQA buffer (BUFFER=YES) but and SVC dump was already in progress.
S237 The error occurred during end-of-volume label verification. Possible causes: Incorrect volume serial Incorrect volume mounted Incorrect labels
S237-04 The block count in the DCB does not match that in the trailer label. A block of data has been misused or skipped.
S237-08 The DSname in a header label does not match that in the JFCB on the second or subsequent volume of a magnetic tape dataset.
S23E The error was detected during execution of a DETACH macro instruction. Either: The parameter passed to detach in register 1 was not a fullword address The storage key of that address did not match that of the issuer of the detach The parameter contained in the addressed fullword of the issuer was not the address of a subtask of the isser of the detach.
S240 An error occurred during execution of a RDJFCB macro.
S240-04 A RDJFCB macro instruction was issued, but the DCB did not contain a foundation extension block.
S240-08 A RDJFCB macro instruction was issued, but no EXLST address was found in the DCB.
S240-0C A RDJFCB macro instruction was issued, but no JFCB exit was specified in the DCB exit list.
S240-10 A RDJFCB macro instruction was issued, but the JFCB buffer is not within the user's storage.
S2F3 Job was being executed when system failure occurred- A system restart was performed.
S300 An error was detected when and I/O operatoin was requested; the storage protection key was not 0 or the DEB validity check routine returned to EXCP wit a non-zero return code. In the abnormal termination dump, the TCB field TCBEXCPD (at offset C0) points to the EXCP problem determination area. The items in the problem determination area of greatest interest to you are: (all offsets are in hex) offset 10 contains a copy of the registers when EXCP determined the error condition.  offset 50 contains the contents of the Request Queue Element (RQE) if allocated, when the program check occurred.
S305 The error occurred during execution of a FREEMAIN macro: The specified subpool could not be found.  The SP parameter was specified but the virtual strage area to be released was not within subpool zero.  The SP parameter was not specified but the virtual storage area to be released was not within subpool zero.  The SP parameter was specified correctly, but the boundaries of the storage areas to be freed were not completely described by a descriptor queue element.
S306 The error occurred during the execution of the LINK, XCTL, ATTACH, or LOAD SERVICE ROUTINES. The authorized routine requested a module, which could bot be found on an authorized library, but a copy of the module may have been found on a non-authorized library.
S306-04 The requested program was not found in the indicated source.
S306-08 An uncorrectable I/O error occurred when the control program attempted to search the directory of the library containing the module.
S306-0C The module could not be found in the LPA or in the LPA directory or an authorized library.
S30A The error occurred during execution of an R-form FREEMAIN macro for one of the following reasons: A FREEMAIN for an entire subpool was requested (register 1 was zero) but the length in register 0 was NT set to zero.  The specified subpool could not be found.  The SP parameter was specified but the virtual storage area to be released was not within subpool zero.  The SP parameter was not specified, but the Virtual Storage Area to be released was not within subpool zero.  The SP parameter was specified correctly, but the boundaries of the storage areas to be freed were not completely described by a descriptor queue element (DQE).
S313-04 (04 is the only possible return code associated with S313). An I/O error occurred reading a format 2 or format 3 DSCB during the execution of an OPEN macro.
S314 I/O error in reading DSCB. SORTIN JCL gave wrong block size for a variable record.
S314-04 An I/O error occurred reading a DSCB for a dataset on a direct access device during execution of a CLOSE macro.
S314-08 An I/O error occurred reading a FORMAT 1 DSCB during execution of a CLOSE macro and standard user labels were specified.
S322 Job or step time exceeded the specified limit. Program is in a loop. Insufficient time parameter on JOB or EXEC card.
S337 The error occurred when the end of a data set was reached. Possible causes: No end of file routine was provided.  Tried to read past end of file.  Tried to write on a tape defined as input.
S337-04 The end of dataset was reached, but no end-of-dataset routine (EODAD) specified in the DCB for DD dummy dataset.
S337-08 No end-of-dataset routine (EODAD) specified in the DCB for DD dummy dataset.
S338 An unauthorized ptask attempted to use authorized options of the ENQ macro instruction.
S378 The error occurred during execution of an RC or RU form FREEMAIN macro. Possible causes: A FREEMAIN for an entire subpool was requested (register 1 was zero) but the length in register 0 was not set to zero.  The SP parameter was specified, but the virtual storage area to be released was not within the subpool specified.  The SP parameter was not specified but the virtual storage areas to be released wit not within subpool zero.  The specified subpool could not be found.  The SP parameter was specified correctly, but the boundaries of the storage area to be freed were not completely described by the descriptor queue element (DQE).
S400 The DCB in the DEB does not equal the DCB address in the IOB. In the abnormal termination dump, the TCB field TCBEXCPD (at offset CO) points to the EXCP problem determination area. The items in the problem determination area of the greatest interest to you are: hex offset 10 contains a copy of the registers when EXCP determined the error condition; hex offset 50 contains the contents of the request queue element (RQE) if allocated when the program check occurred.
S413 INPUT, INOUT, or RDBACK specified, but no vol ser in DD; or I/O error in reading volume label; or could not mount volume on device; or volumes specified less than devices allocated. Possible causes: Forgotten volume serial for input tape.  Had DISP new when should have had OLD.  Generated as NL, tried to read as SL.  Missing or inconsistent DCB information.  Volume could not be mounted so operated mounted scratch.  Tried to close a file without opening it.  Tried to open a second dataset on a tape without closing the first.  The requested drive was switched off.  SORT verb blew due to SD not matching FD with using or giving.
S413-04 Possible causes: No unit is available for mounting the volume for the dataset being opened.  The volume already on the allocated unit as specified by the VOL=SER is either permanently resident or reserved.  It could not be demounted in order to mount the required volume or the volume cannot be demounted because another DCB is open on that device or the device type is incompatible with the DSORG in the DCB.  This error may be due to a previous abnormal termination associated with the same unit inthe same step.
S413-08 An I/O error occurred positioning a magnetic tape volume.
S413-0C An I/O error occurred reading the volume label on a magnetic tape volume.
S413-10 An I/O error occurred writing a tape mark.
S413-18 The specified dataset was opened for input but no volume serial number was specified on the DD statement.
S413-1C An OPEN macro was issued for a dataset, but the volume sequence number on the associated DD statement was greater than the number of volumes containing the dataset.
S413-20 An I/O error occurred reading the volume label on a direct access volume.
S413-24 An OPEN macro was issued for a dataset on magnetic tape. A density was specified in the DCB DEN parameter which was incompatible with the recording density of the drive allocated to the dataset.
S413-34 LABEL=(N) was specified, where N is greater than 1, and VOL=SER was not specified for a tape dataset.
S513-04 (04 is the only possible return code associated with S513) an OPEN macro was issued for a magnetic tape dataset allocated to a device that already has an open dataset on it.
S513-08 Label violates published STDS….is rejected.
S522 Job or TSO session exceeded maximum job wait time or operator did not mount the required tape within allowed time limit. Waiting on datasets, may requeue later.  S604 Possible Causes: GETMAIN error.  Missing SORTLIB card.  Subscript error.  Clobbered free queue element.
S605 Freemain error, see S604.
S60A Freemain queue element or address error. Possible Causes: Needs more core.  JCL for input disks requested 2 units, gave 1 volume serial.  Missing DD card for SYS1.SORTLIB.
S613 I/O error in tape positioning or label processing. Possible Causes: Tape label was not in requested density.  DCB missing.  DEN missing on a tape that requires it default DEN=3 (1600 BPI).  RECFM=F was specified for a file which was FB.  Incorrect header.  Tape positioning error.  Tape drive failure during OPEN.
S613-04 An I/O error occurred positioning a magnetic tape volume.
S613-08 An I/O error occurred reading a label on a magnetic tape.
S613-0C An invalid label was read from a magnetic tape volume. This error may be due to a previous abnormal termination associated with the same tape since it was last mounted, possibly in a previous job or step, leaving the tape positioned improperly.
S613-10 An I/O error occurred writing a tape label.
S613-14 An I/O error occurred writing a tape mark after the header labels.
S614 Uncorrectable I/O error occurred in writing end-of-file during close processing a dataset on a direct access device or the operator dismounted volume while program was processing.
S614-04 An I/O error occurred writing a file mark for a dataset on a direct access device during execution of a CLOSE macro.
S614-08 A file mark should have been written on an output dataset. The DCBFDAD field in the DCB indicated an extent number in the DEB greater than the number of extents in the dataset. Consequently, it could not be determined where the file mark should have been written.
S622 TSO session was cancelled. Possible Causes: Operator stopped TSO or cancelled the user.  User signaled attn after the allocation process had completed.  The user disconnected his terminal from the system.
S637 I/O error in writing tape mark, tape positioning, reading label, sensing for file protection ring; DCB bit does not indicate concatenation of unlike attributes.
S637-04 An I/O error occurred while reading a tape label, writing a tape mark, or positioning a magnetic tape volume.
S637-08 Following user trailer processing, an I/O error occurred positioning a magnetic tape.
S637-0C Concatenation of datasets with unlike attributes was detected, but not specified in the DCB.
S637-10 An I/O error occurred while positioning a magnetic tape dataset that was opened with the option input or inout to be read backward. If it is a tape with standard labels, the error occurred positioning at the labels. If it is a tape with no labels, the error occurred positioning at the data.
S637-14 An I/O error in tape positioning occurred for a dataset with the leave option specified in the OPEN macro or in the FEOV macro.
S637-18 An I/O error in tape positioning occurred for a dataset opened with the reread option.
S637-1C An I/O error in tape positioning occurred when FEOV was issued for a dataset with DISP=PASS and no open option 2 specified.
S637-24 An I/O error occurred rewinding a scratch magnetic tape volume. Either FEOV with a rewind option was issued, or no open OPTION 2 was specified when the disposition was not PASS.
S637-2C An I/O error occurred while rewinding a magnetic tape volume prior to verifying the volume label.
S637-34 An I/O error occurred during end of volume processing while reading the volume label of a magnetic tape
S637-38 An I/O error occurred while positioning a tape without labels or with nonstandard labels.
S637-3C An I/O error occurred while positioning a concatonated magnetic tape dataset.
S637-40 An I/O error occurred positioning a magnetic tape dataset that was opened with the option input or input to be read forward.
S637-44 An I/O error occurred while checking sense bytes to determine if a file protect ring is on a magnetic tape containing a dataset opened or inout.
S700 A program check occurred during EXCP processing of an I/O request. The program check occurred in a supervisor service routine called by EXCP. This is likely not a programmer error. In the abnormal termination dump, the TCB field TCBEXCPD (at offset C0) points to the EXCP problem determination area. The items of greatest interest to you are: Hex offset 02 contains a flag byte indicating where the error occurred.  Bit 1 = 1 means error in SVC portion of the EXCP; Bit 2 = 1 means error in SRB portion of the EXCP; Bit 3 = 1 means error in PCI appendage; Bit 4 = 1 error in CHE appendage; Bit 5 = 1 means error in ABE appendage; Bit 6 = 1 means error in EOE appendage; Bit 7 = 1 means error in PGFX appendage; Bit 8 = 1 means appendage is active; No bits on means error in SIO appendage.  Hex offset 04 contains a copy of the program status word before RTM was entered.  Hex offset 0E contains the interruption code.  Hex offset 10 contains a copy of the registers when EXCP issued the abend macro.  Hex offset 54 contains the contents of the request queue element, if allocated, for the I/O request being processed.
S706 The requested load module was marked by the linkage editor as not executable. Bad prior LIKDEDIT -check the LKED SYSPRINT.
S706-04 Improper program linkage (NON-IMS pgm linked used LNKTESTI Clist)
S713 Tried to write on a dataset whose data protection had not expired. Operator replied 'M' to IEC507D to honor exp date.
S713-04 A dataset on magnetic tape was opened for inout, outin, output, outinx, or extend, but the volume contained a dataset whose expiration date had not been reached.
S713-08 An OPEN macro was issued with inout for a dataset on a direct access device with DISP=OLD specified on the DD statement. The expiration date on the dataset had not been reached.
S714 I/O error in label processing -close for magnetic tape tape drive failure during close.
S714-04 An I/O error occurred writing trailer label 1 for a dataset on magnetic tape during execution of a CLOSE macro.
S714-08 An I/O error occurred writing trailer label 2 for a dataset on magnetic tape during execution of a CLOSE macro.
S714-0C An I/O error occurred writing a tape mark during execution of a CLOSE macro.
S722 The output limit specified by the OUTLIM keyword on the sysout DD statement or by the lines keyword on the jobparm DD statement was exceeded.
S737 I/O error; DSCB not found for multi-volume or concatenated data set. Be sure all the data sets exist for concatenated data sets.
S737-04 An I/O error occurred reading or writing a DSCB during end of volume processing.
S737-08 An I/O error occurred reading a direct access volume label during end of volume processing.
S737-0C An error occurred reading the DSCB for a concatenated partitioned dataset.
S737-10 An I/O error occurred writing a file mark for a dataset on a direct access device.
S737-1C An I/O error occurred while reading a format 3 DSCB.
S737-24 A missing member name was detected by BLDL while searching for the TTR of a concatenated member.
S737-2C The error occurred when a FEOV macro was issued while attempting to write a file mark at the end of data. The DCBFDAD field in the DCB indicated an extent number in the DEB greater than the number of extents in the dataset. Consequently it could not be determined where the file mark should have been written.
S738 An unexpected error occurred during the execution of an ENQ macro. Related information is recorded in SYS1.LOGREC.
S800 An error occurred when EXCP attempted to fix a page for the EXCP request.
S804 Request for 0 bytes of main storage or not enough main storage available. Program exceeded region size.
S806 Possible causes: Load module not found in loadlib.  BLDL detected error.  Module not found or I/O error during directory search.  Missing JOBLIB or STEPLIB card.  Tried to execute a non-existent program.  Tried to execute in batch a program assembled with 'test' option.  SYSIN described incorrectly to LKED or name card missing.  Also, check if '**RACF** is missing or mispositioned on the jobcard.
S806-04 Module not found. The program entry point specified was not found in the indicated library (private library, job library, or link library).
S806-08 An uncorrectable input/output error occurred when the BLDL control program routine attempted to search the directory of the library that contained the program whose entry point was specified. This can occur if the indicated library is an uninitialized partitioned dataset.
S806-0C A SVC routine required by the system could not be found in the link pack area.
S80A Request for 0 bytes of main storage or not enough main storage available. Need more core in region.
S813-04 (04 is the only possible return code associated with S813.) Open error. Possible causes: Incorrect dataset name.  An OPEN macro was issued for a dataset on magnetic tape, but the dataset name on the header label did not match that in the JFCB (Tape's been reused).  Wrong DSname or volumeserial -JCL disagrees with label.  Incorret record format or blocksize; The requested drive is not switched to this machine.
S822 A region required to run the step could not be obtained. One of the following messages will be written to the programmer, depending upon wheather the job was an ordinary job or a deferred checkpoint restart: IEF085I Region Unavailable, Error Code=CDE.  IEF086I Region Unavailable For Restart, Error Code=CDE.
S822-08 IEFO85I - A V=V region was requested and a region size was specified which was larger than the private area, or a V=R region was requested and a region size greater than the V=R area was specified. IEF1861 - The region parameter was increased so that the region could not be obtained.  For ADDRESPC=REAL, the size of the real area was decreased.  For ADDRSPC=VIRT, the size of the private area decreased because the size of the nucleus increased or the size of the SQA or the IPA increased.
S822-16 IEF085I - A V=R area was requested, but either long-fixed or damaged pages in the V=R area made it impossible to obtain the requested region, or a V=R region was requested and there was not enough SQA available for the system to complete the processing of the request; IEF186I - If a REAL region was requested, either long-fixed or damaged pages in the REAL area made it impossible to obtain the required region.
S822-20 IEF085I and IEF186I - Either a V=V or V=R region was requested fragmentation by LSQA, SWA, or subpools 229 or 230 has made it impossible to obtain the requested region.
S822-24 IEF085I and IEF186I -A request for a V=R region could not be satisfied because the installation GETPART exit routine rejected the request.
S837 Error during End-Of-Volume processing for a sequential dataset.
S837-04 A density conflict exists between the user-specified density and the unit's density capability.
S837-08 Specify more volume serial numbers or a larger volume count in the VOL parameter of the DD statement.
S837-0C Tape volume was requested and mounted but another dataset was processing the volume.
S878 GET MAIN error not enough virtual storage on region statement. Try a larger REGION parm on the JOB CARD.
S906 IMS use count limit error.
S90A The error occurred during the execution of an R-form FREEMAIN macro. The address of the storage area to be relesed was not on a doubleword boundary (A multiple of 8).
S913 RACF security, Trying to access to a dataset not authorized to use. The error occurred during 1) The execution of an OPEN macro or during end-of-volume processing for a password protected dataset, or 2) the execution of an OPEN macro involving a checkpoint dataset.  Operator failed to supply correct password for a protected dataset.  Unauthorized attempt to use LABEL=BLP.  Previous dataset on this tape protected, new dataset is not protected.
S913-04 An OPEN macro was issued for a magnetic tape dataset with American National Standard labels. The volume accessability byte (offset X'OA') in the volume label is not blank. This indicates the label was not written for use on an IBM system, or that it was written by the user. The volume must be recreated.
S913-08 An OPEN macro was issued for a magnetic tape dataset with american national standard labels. The security byte in the header label was not bland and not equal to X'F1'. This means the label either was not created on an IBM system or was created by the user. The volume must be recreated for use on an IBM system.
S913-0C An OPEN macro was issued for a protected datset for which you are not allowed this type of access.
S913-10 An OPEN macro was issued to the VTOC for output processing by an unauthorized job step or job-step task.
S913-14 An OPEN macro was issued to concatenate checkpoint and noncheckpoint datasets.
S913-18 An open TYPE=J macro was issued for a magnetic tape volume. The JFCB was modified to indicate LABEL=BLP (Bypass label processing) and the task was not authorized. BLP may be specified in the JCL (if the installation reader procedure allows it), but the JFCB may not be modified to indicate BLP unless the task is authorized.
S913-1C The error occurred during the execution of an open TYPE=J macro to a direct access device dataset. The dataset name supplied to open was not available to the job. Either the dataset was bein opened for input and some other job had exclusive control of it, or the dataset was being opened for an option other than input (thus requiring exclusive control) and some other job was using the dataset.
S913-20 An OPEN macro using the EXCP access method was issued in which user-written appendages were required. The appendage names were not included in the parmlib member IEAAPPOO, and the program issuing the open was not authorized (by APF or protect key.).
S913-28 An OPEN macro was issued for a checkpoint dataset. The dataset organization was not BPAM or BSAM and the task was not authorized via the authorized program facility (APF).
S913-2C An OPEN macro was issued to an ISAM dataset defined by two or three DD statements. Either the dataset names coded in the DD staements were not all the same, or the JFCB passed to open (if an open TYPE=J is being used) has a dataset name different from that coded in the DD statements.
S913-30 An OPEN macro was issued to write a daaset on a magnetic tape containing one or more previous datasets. The protection mode of the dataset to be written was different than the protection mode of the previous dataset.
S913-38 An OPEN was issued for a RACF-protected dataset to which the user was not authorized.
S913-3C An OPEN was issued for a dataset with a Format-1 DSCB indicated RACF protection, but the dataset is not defined to RACF.
S913-40 A VSAM data space being opened is RACF-defined.
SA00 A program check occurred in an appendage. In the abnormal termination dump, the TCB field TCBEXCPD (at offset CO) points to the EXCP provided debugging area. The items in the debugging area of greatest interest to you are: Hex offset 2 contains a flag byte indicating where the error occurred.  Bit 1 = 1 means error in SVC portion of the EXCP; Bit 2 = 1 means error in SRB portion of the EXCP; Bit 3 =1 means error in PCI appendage; Bit 4 = 1 error in CHE appendage; Bit 5 = 1 means error in ABE appendage; Bit 6 = 1 means error in EOE appendage; Bit 7 = 1 means error in PGFX appendage; Bit 8 = 1 means appendage is active; No bits on means error in SIO appendage.  Hex offset 04 contains a copy of the program status word before RTM was entered.  Hex offset 0E contains the interruption code.\ Hex offset 10 contains a copy of the registers when EXCP issued the abend macro.  Hex offset 54 contains the contents of the request queue element, if allocated, for the I/O request being processed.
SA0A Inactive program overlaps overlaps free area; area to be released overlaps a free area.
SA13 The error occurred during execution of an OPEN macro on magnetic tape.
SA13-04 An unexpected load point was encountered whil positioning a tape. For NL tape this is probably a user error associated with the use of a mutlivolume multfile NL tape.
SA13-08 The requested file sequence number is less than that of the first file on the SL tape during an open to the start of the file.
SA13-0C The requested file sequence number is less than that of the first file on the SL tape during an open to the end of a file.
SA13-10 A tape mark was read instead of a HDR1 label while forward spacing to the desired file on an SL tape. The multifile tape ends before the desired file. When positioning to the end of file 1, this means the vol label is followed by a tape mark. Check the file sequence number and the volume serial numbers, and that the job that wrote the tape wrote all the files.
SA13-14 A tape mark was read instead of a HDR1 label while opening for input to the start of the desired file on an SL tape. Thus, the tape ends just before the diesired file. Check the file sequence number and the volume serial numbers and that the job that wrote the tape wrote all the files.
SA13-18 An EOV1 label was read on the last SL tape volume while forward spacing to the desired file. If opening to the end of the file, it could not be treated as the end of the dataset because it was for a previous file sequence number.
SA37 The error occurred during end of volume processing. The task is terminated unless the error is to be ignored as specified in the DCB abend exit routine. Possible causes: An open DCB may have been partially overlaid.  The DCB may have been closed in a SYNAD routine.  The DCB may have been automatically closed by a previous End Of Volume error where ignor was specified in the DBC abend exit.
SA37-04 An SVC 55 (EOV) was issued, usually by a check, get, or put routine, against a DCB which was not open.
SA37-08 The data extent block (DEB) does not point to the DCB.
SA78 The error occurred during the execution of an RC or RU form FREEMAIN macro: Possible causes are: The control program found that the address and length specifications in the release request defined an area to be freed that overlapped a free area in virtual storage.  Part of the area being freed is still fixed in real storage. Fixed storage blocks cannot be freed.  SACC Not an error - FORTRAN accounting termination.
SB00 A program check occurred in an EXCP procedure. In the abnormal termination dump, the TCB field TCBEXCPD (at offset CO) points to the EXCP provided debugging area. The items in the debugging area of greatest interest to you are: Hex offset 2 contains a flag byte indicating where the error occurred.  Bit 1 = 1 means error in SVC portion of the EXCP; Bit 2 = 1 means error in SRB portion of the EXCP; Bit 3 = 1 means error in PCI appendage; Bit 4 = 1 error in CHE appendage; Bit 5 = 1 means error in ABE appendage; Bit 6 = 1 means error in EOE appendage; Bit 7 = 1 means error in PGFX appendage; Bit 8 = 1 means appendage is active; No bits on means error in SIO appendage.  Hex offset 04 contains a copy of the program status word before RTM was entered.  Hex offset 0E contains the interruption code.  Hex offset 10 contains a copy of the registers when EXCP issued the abend macro.  Hex offset 54 contains the contents of the request queue element, if allocated, for the I/O request being processed.  Hex offset 80 is the start of the 160 byte blocks involved in the I/O request, if allocated.
SB0A The error occurred during execution of an R-form GETMAIN or FREEMAIN macro. Possible causes are: A subpool number greater than 127 was specified by a problem program (a program not authorized to use valid subpool numbers greater than 127).  An authorized program requested an invalid subpool.  Tried to change blocking factor while loading a dataset.  Control passed beyond end of program due to an invalid PERFORM.
SB14 At close a partitioned data set directory cannot be updated because: the name is already in the directory or no space is available in the directory or an I/O error was encountered in the directory.  Possible cause: Allocated directory space in JCL, written as sequential dataset.
SB14-04 A duplicate name was found in the directory of the PDS.
SB14-0C The attempted update of the partitioned dataset found that there was no space left in the directory.
SB14-10 An I/O error occurred trying to update the directory of the partitioned dataset.
SB14-14 The close routine attempted to update the directory of the partitioned dataset, however the DCB of the dataset was not open.
SB14-18 Unsuccessful GETMAIN for stow workarea when close tried to update a partitioned dataset. Region size is too small.
SB37 Space problem, usually on input or output dataset. The data set on DASD output already had 16 extents, but required more space or secondary space was too small or no more space was available on the volume or at end of volume, the volume must be demounted, but the system is unable to dismount the volume.
SB37-04 During end-of-volume processing the system had to demount a volume in order to mount the next volume of the dataset. It was unable to demount the volume for one of the following reasons: The volume was permanently resident or was reserved.  Another job had datasets allocated on the volume.  The failing task had open datasets on the volume.  For an output dataset on a DASD no more space was available on the volume.  16 extents already obtained for the output dataset but more space is required.  VTOC is full.  For an output dataset on a tape volume, volume needed to be demounted because the reflective spot was encounted and more records needed to be written, but the limit of output tape volumes had been reached.
SB37-08 During end-of-volume processing the system attempted to extend the dataset to a volume on which the DIRF bit was set. The VTOC for the volume could not be converted to the standard format for one of the following reasons: Two datasets were allocated to the same space on the volume.  A split cylinder dataset was located on the same cylinder as a non-split cylinder dataset.  The VTOC conversion routine is set to reject DIRF requests.
SB37-0C The mounted direct access volume was requested to continue processing the dataset, but the unit already contained the maximum of 127 concurrent users.
SC03 A data set could not be closed by the control program, because the DCB had been erroneously modified. ISAM file -Bad block size.
SC13 The error occurred during the execution of an OPEN macro for a concatenated partitioned or graphics dataset. Attempted to write output to concatenated partitioned datasets missing or deleted joblib data set. Possible Cause: Graphics -system problem-wait for IPL.
SC13-04 The current task tried to open a graphics device that was previously opened and not closed.
SC13-10 An OPEN macro was issued specifying output or extend for a concatenated partitioned dataset, output datasets cannot be concatenated.
SD0D Invalid abend recursion during abnormal termination of subtask job step task terminated.
SD13 Open for graphics -DCB for other than graphics device.
SD23 The error ocurred during the execution of a WTO or WTOR macro for one of the following reasons: The parameter list supplied to the WTOR macro does not begin on a fullword boundary.  A WTOR/MLWTO parameter list was specified.  A multiline WTO was specified and space was not available in subpool 229 for a workarea for SVC 35.  The parameter list passed by the user does not reside instorage that is accessible by the user.  Space was not available in subpool 231 for an ORE or WQE buffer.
SD2D Overlay supr. found invalid record type bad load module. Re-linkedit.
SD37-04 Space problem, usually in load library. (04 is the only possible return code associated with SD37) A dataset opened for output used all the primary space, and no secondary space was requested. Either specify a larger primary quantity or add a secondary quantity to the request. Try increasing the primary SPACE allocation.
SE37 Space problem, usually in a PDS. The error occurred during end of volume processing when an output operation was requested for a dataset. Ran out of directory space in a PDS or output exceeded volume count.
SE37-04 A dataset opened for output used all space available on the current volume, and no more volumes were available: Not enough volumes were specified for the dataset through the 'SER', volume count, or 'REF' subparameter of the volume parameter.  When all the volumes were filled, the program attempted to write another record.  For a partitioned dataset, all space was filled when the program attempted to write another record 16 extents had been used when the program attempted to write another record, however no volume was available for demounting.
SE37-08 On a dataset opened for output, end-of-volume had found a DSCB with a duplicate dataset name on the next volume, with a volume sequence number less than that in the DEB.  A multi-volume physical sequential dataset was being written on a direct access device all space was filled on a volume and an attempt was made to obtain space on the next specified volume but space either was not available on that volume or the dataset already existed on that volume.
SF2D Overlay supervisor - Invalid Supervisor call. Bad Load Module. Re-LNKEDT entire module.
SF37 Hardware error.
U0004 GO step of FORTRAN - subrountine fileno - non sequential dataset.
U0008 GO step of FORTRAN - subrountine fileno - IDSRN out of range.
U0012 GO step of FORTRAN - subrountine fileno - dataset reference number has not been used.
U0016 Standard abend code for SYNC SORT failure. See diagnostic messages.  GO step of FORTRAN - Missing SD4060 DD card for SD4060 output.  GO step of FORTRAN - subroutine fileno - second argument not 'IN' or 'OUT'.
U0020 GO step of FORTRAN - subroutine fileno - previous file not closed.  ASMF could not open SYSIN. Check the SYSIN DD card.  I/O failure reading a bad track.
U0024 GO step of FORTRAN - subroutine fileno - device is not a tape.  RPG - alphanumeric data in numeric-specified field.  RPG - missing DD card.
U0030 GO step of FORTRAN - missing FT06F001 DD card.
U0040 RPG - input file out of sequence.
U0044 RPG - undefined record type.
U0064 Archived or inactive GDG.  RPG - QSAM I/O Error.
U0100 FDR - open error - unable to open disk or tape file.
U0101 FDR - disk I/O Error.
U0200 FDR - tape I/O Error.
U0201 FDR - tape End-Of-File before dataset or trailer record found.
U0204 PAN#8 - SYSPRINT DD statement missing.
U0240 Possible program looping. Program time out due to looping problem.  FORTRAN - SPIE.
U0261 Improper program linkage (IMS program linked used LNKTEST Clist); IMS program not linked using LNKTESTI (consider this first, but other reasons are possible).
U0402 FDR - SYSPRINT or SYSPRIN-N error.
U0428 PSB not found. No IMS gen. U456 Program stopped.
U0452 Transaction stopped. SUGGESTION: Restart using IMSRM.
U0456 Program/PSB stopped. SUGGESTION: Restart using IMSRM.
U0457 The same program is being run in two different jobs concurrently.
U0458 Database stopped.
U0474 Maximum time.; Message region stopped - contact data center.
U0476 Invalid PSB or no PSB. SUGGESTION: Check IMSGen and PSBDump.  Data Exception, Non numeric data in numeric field. See S0C7.
U0502 FDRDSF - Input control statement error.
U0519 Missing GO BACK, EXIT or STOP RUN.
U0688 IMS not active. SUGGESTION: Contact Tech Support.  JOB cancelled (JOB ran in the wrong JOB class). SUGGESTION: Rerun job with CLASS=J.
U0775 BMP program abended due to exceeding IMS calls between checkpoints.  Program has made too many calls without taking a checkpoint.
U0777 IMS step lock out.
U0778 Blocksize or LRECL problem; See S013
U0844 Production database out of space.
U0852 Another concurrent IMS job has the database locked for update. SUGGESTION: Rerun your job later.  Batch program is accessing a database that is being updated. SUGGESTION: Try rerunning the job later.
U0888 FDR - Diagnostic warning associated with text on SYSPRINT.
U0999 SYNCSORT - I/O error has occurred. See Diagnostic Messages U2000-.
U3303 Database stopped.
U3699 Invalid dump code used. Outside abend code range.
4000 PL/1

</pre>

<br><br>
January 2025
