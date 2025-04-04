# CBT558
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 558 is from Dick Thornton, who is the author of the       *   FILE 558
//*           DISASSEMBLER program on File 217, and his new         *   FILE 558
//*           DISASSEMBLER program on File 234.  This is a large    *   FILE 558
//*           collection of his Assembler code.  There are some     *   FILE 558
//*           interesting and unique programs to be found here.     *   FILE 558
//*           Please see member $$NOTE1 for details about some      *   FILE 558
//*           of them.  See member $MACLIB for some macros needed.  *   FILE 558
//*                                                                 *   FILE 558
//*           emails:  (check to see which are relevant):           *   FILE 558
//*               dickthor@hotmail.com                              *   FILE 558
//*               cthornton@swva.net                                *   FILE 558
//*               rthornton@trigon.com                              *   FILE 558
//*                                                                 *   FILE 558
//*        Dick Thornton's total submission consisted of 15 pds'es  *   FILE 558
//*        which he refers to by name.  These pds'es may all be     *   FILE 558
//*        found within his 8 files on this tape:  Files 558 thru   *   FILE 558
//*        565.  Below is a map which tells you on which CBT Tape   *   FILE 558
//*        file, each of Dick's "named pds'es" may be found:        *   FILE 558
//*                                                                 *   FILE 558
//*        Named PDS         CBT Tape File containing it            *   FILE 558
//*        ---------         ---------------------------            *   FILE 558
//*        ASM               File 558                               *   FILE 558
//*        C (Language)      File 559                               *   FILE 558
//*        SAMPSRC           File 559    (as member $SAMPSRC)       *   FILE 558
//*        JCL               File 560                               *   FILE 558
//*        CLIST             File 561                               *   FILE 558
//*        EXEC              File 562                               *   FILE 558
//*        MSGS              File 562    (as member $MSGS)          *   FILE 558
//*        PLIB              File 562    (as member $PLIB)          *   FILE 558
//*        COBOL             File 563                               *   FILE 558
//*        DATA              File 564    (as member DATA)           *   FILE 558
//*        INSTRUCT          File 564    (as member INSTRUCT)       *   FILE 558
//*        MEMORY            File 564    (as member MEMORY)         *   FILE 558
//*        CLASS             File 565    (as member COBCLASS)       *   FILE 558
//*        CCLASS            File 565    (as member CCLASS)         *   FILE 558
//*        DUMPCLS2          File 565    (as member DUMPREAD)       *   FILE 558
//*                                                                 *   FILE 558
//*        Each file in this collection is being equipped with a    *   FILE 558
//*        $$README member, to help you see what the contents       *   FILE 558
//*        of that file are about.                                  *   FILE 558
//*                                                                 *   FILE 558
//*        Please see member $$NOTE1 on this file, which describes  *   FILE 558
//*        some especially useful and unique programs which may     *   FILE 558
//*        be found in this collection.  See member $$NOTE2 also.   *   FILE 558
//*                                                                 *   FILE 558
//*        Extra macros were added, because they seemed to be       *   FILE 558
//*        missing in the originally submitted file.  See member    *   FILE 558
//*        $MACLIB2, as well as member $MACLIB.   (SG 11/22/02)     *   FILE 558
//*                                                                 *   FILE 558
//*        The following is a list of members of this file:         *   FILE 558
//*                                                                 *   FILE 558
//*        $COMMAND   01.01  1999/05/20  8:35     36  BC0THOR       *   FILE 558
//*        ABAL       01.04  2002/04/02 16:10    498  BC0THOR       *   FILE 558
//*        ABDUMP     01.01  1999/08/17 14:04      9  BC0THOR       *   FILE 558
//*        ABENDJOB   01.04  2001/10/03 17:17     74  BC0THOR       *   FILE 558
//*        ABEND878   01.11  1996/03/29 15:51    670  BC0THOR       *   FILE 558
//*        ALIAS      01.32  1992/04/20  9:56    790  USER02        *   FILE 558
//*        ALIASES    01.07  2000/03/07 16:16    119  BC0THOR       *   FILE 558
//*        ALIAS2     01.00  2000/03/07 14:46     69  BC0THOR       *   FILE 558
//*        ALLDSNS    01.52  2002/01/23 16:40    692  BC0THOR       *   FILE 558
//*        ALLOCDYN   01.34  2000/10/10  9:55   1690  BC0THOR       *   FILE 558
//*        ARCHVDMP   01.17  1992/06/15 14:47    519  USER02        *   FILE 558
//*        ASCBLIST   01.02  1990/11/27 10:25    100  USER02        *   FILE 558
//*        ASC2EBCD   01.11  2001/02/12  9:14    331  BC0THOR       *   FILE 558
//*        ASMMAIN    01.03  2001/08/17 15:57    161  BC0THOR       *   FILE 558
//*        ASMSUBD1   01.04  2001/08/17 15:56    129  BC0THOR       *   FILE 558
//*        ASMSUBS1   01.04  2001/08/17 15:54    130  BC0THOR       *   FILE 558
//*        ASM31SUB   01.02  1993/08/19 11:03     65  USER02        *   FILE 558
//*        A31BIT     01.02  1991/11/07  9:29     79  USER02        *   FILE 558
//*        BAGETE     01.09  2002/01/31 13:39    428  BC0THOR       *   FILE 558
//*        BLDCNTL    01.01  2001/05/23 13:46     98  BC0THOR       *   FILE 558
//*        BUILDTBL   01.03  2001/04/12 12:39    309  BC0THOR       *   FILE 558
//*        CALLGND2   01.00  2002/01/30 14:33    188  BC0THOR       *   FILE 558
//*        CALLGND3   01.09  2001/01/05 15:09    291  BC0THOR       *   FILE 558
//*        CALLPDSR   01.02  2000/02/25  9:58    174  BC0THOR       *   FILE 558
//*        CALLQIO1   01.13  2001/03/29 11:02    260  BC0THOR       *   FILE 558
//*        CALLQIO2   01.17  2001/07/24 16:49    260  BC0THOR       *   FILE 558
//*        CALLRDLM   01.13  2002/02/18 14:49   1334  BC0THOR       *   FILE 558
//*        CALL095    01.01  2001/11/29 14:05     97  BC0THOR       *   FILE 558
//*        CAMLST     01.04  1999/03/19 16:34     78  BC0THOR       *   FILE 558
//*        CATALOGD   01.03  1999/03/19 16:24     94  BC0THOR       *   FILE 558
//*        CATLGLST   01.12  2002/01/30 10:17    471  BC0THOR       *   FILE 558
//*        CBRAKETS   01.05  2000/10/09 16:10     68  BC0THOR       *   FILE 558
//*        CHECKVBS   01.02  2002/01/19 22:41    174  BC0THOR       *   FILE 558
//*        CHGDDNM0   01.00  2001/12/04 10:26    158  BC0THOR       *   FILE 558
//*        CHGJOBCD   01.06  1998/07/06 15:06    177  BC0THOR       *   FILE 558
//*        CHGJOBNM   01.01  1990/04/11  7:44    113  USER02        *   FILE 558
//*        CHGUNIT    01.09  1990/10/16 15:25    109  USER02        *   FILE 558
//*        CHKVOLS    01.02  1992/07/31 12:39    772  USER02        *   FILE 558
//*        CHRCOPY    01.01  1989/09/26  8:23   2722  USER02        *   FILE 558
//*        CHRDUMP    01.52  2001/03/30 12:57   3209  BC0THOR       *   FILE 558
//*        CICSSCAN   01.07  2000/08/07 15:37    174  BC0THOR       *   FILE 558
//*        CLISTMON   01.07  2000/05/10 14:25    151  BC0THOR       *   FILE 558
//*        CLONETAP   01.00  1992/04/02  9:35    176  USER02        *   FILE 558
//*        CLRSCN     01.00  1989/09/26  8:24     28  USER02        *   FILE 558
//*        CMPRDIR    01.04  2001/05/18 16:56    162  BC0THOR       *   FILE 558
//*        COBABEND   01.01  2001/07/11  8:45     49  BC0THOR       *   FILE 558
//*        COBLSETY   01.03  2000/01/28 12:16    148  BC0THOR       *   FILE 558
//*        COBLSUBR   01.04  2000/01/28 12:18    138  BC0THOR       *   FILE 558
//*        COBLTYPE   01.22  2002/02/25 11:20    568  BC0THOR       *   FILE 558
//*        COBLTYP2   01.04  2000/01/28 12:11     97  BC0THOR       *   FILE 558
//*        COBRDLST   01.11  2000/01/28 13:47    240  BC0THOR       *   FILE 558
//*        COBREAD    01.06  2000/08/14 11:49   1248  BC0THOR       *   FILE 558
//*        COBSUBEM   01.09  2000/01/28 12:28    280  BC0THOR       *   FILE 558
//*        COB2ASM    01.57  1989/09/26  8:24    983  USER02        *   FILE 558
//*        COB2EP     01.00  2001/12/13  7:50     34  BC0THOR       *   FILE 558
//*        COB2MAIN   01.00  2001/12/17 13:55   1152  BC0THOR       *   FILE 558
//*        COB2TGT    01.00  2001/12/13  9:58    167  BC0THOR       *   FILE 558
//*        COMPARE    01.02  2000/04/25 10:32     78  BC0THOR       *   FILE 558
//*        COMPASM    01.01  2001/11/09 13:34    106  BC0THOR       *   FILE 558
//*        COMPCBL    01.00  1989/09/26  8:25     98  USER02        *   FILE 558
//*        COMPRMEM   01.02  2000/02/22  9:05    229  BC0THOR       *   FILE 558
//*        CONCAT     01.00  1989/09/26  8:25     16  USER02        *   FILE 558
//*        COPY       01.24  2000/07/31 16:24    150  BC0THOR       *   FILE 558
//*        COPYDUMP   01.20  2001/01/15 10:26    218  BC0THOR       *   FILE 558
//*        COPYMULT   01.01  1991/01/25  8:21    184  USER02        *   FILE 558
//*        COPYNUM    01.02  2001/01/25 12:28    105  BC0THOR       *   FILE 558
//*        COPYV      01.06  2002/01/19 17:37     86  BC0THOR       *   FILE 558
//*        COUNTREC   01.08  1999/08/17 10:02    355  BC0THOR       *   FILE 558
//*        CPUID      01.02  1993/07/19 16:26     61  USER02        *   FILE 558
//*        CSECTLST   01.06  2001/11/26  9:33    574  BC0THOR       *   FILE 558
//*        CSECTMCH   01.09  2000/11/15  9:12    231  BC0THOR       *   FILE 558
//*        CSECTMRG   01.04  2000/11/15 13:55    139  BC0THOR       *   FILE 558
//*        CTLGLIST   01.05  1993/06/08  9:04    134  USER02        *   FILE 558
//*        CURRDATE   01.01  2002/01/23 11:14    195  BC0THOR       *   FILE 558
//*        CURRVOL    01.02  1993/11/30 10:50     73  USER02        *   FILE 558
//*        CVTCLIST   01.01  2001/04/05 19:11   1236  BC0THOR       *   FILE 558
//*        DDLIST     01.02  1989/08/10 15:16    162  USER02        *   FILE 558
//*        DELEJSPC   01.03  1999/05/14 16:29     88  BC0THOR       *   FILE 558
//*        DESERV     01.07  2002/02/07 18:46    186  BC0THOR       *   FILE 558
//*        DISASM0    01.03  2002/02/07 18:32   1590  BC0THOR       *   FILE 558
//*        DISASM1    01.03  2002/02/07 18:32   2051  BC0THOR       *   FILE 558
//*        DISASM2    01.02  2002/02/07 18:33   2553  BC0THOR       *   FILE 558
//*        DISASM99   01.25  2001/12/20 10:14    646  BC0THOR       *   FILE 558
//*        DISKCTLG   01.00  1992/04/06 15:34    389  USER02        *   FILE 558
//*        DISTEST    01.04  2002/03/25  9:06    442  BC0THOR       *   FILE 558
//*        DLITCBL    01.06  2001/04/08 12:35    225  BC0THOR       *   FILE 558
//*        DSNUPDAT   01.00  1998/07/06 16:23    411  BC0THOR       *   FILE 558
//*        DSNVOLS    01.03  1998/12/28 15:38    203  BC0THOR       *   FILE 558
//*        DUMP       01.08  1990/12/10 15:18    130  USER02        *   FILE 558
//*        DUMPFIL    01.00  1998/07/06 16:24   1582  BC0THOR       *   FILE 558
//*        DUMPSTOR   01.06  2001/11/29 15:54    441  BC0THOR       *   FILE 558
//*        DUPLMEMB   01.02  2002/04/03 13:51    156  BC0THOR       *   FILE 558
//*        DYNERRS    01.01  1993/09/16 14:09    171  USER02        *   FILE 558
//*        EASTER     01.04  1990/11/28 11:59    267  USER02        *   FILE 558
//*        EBCD2ASC   01.04  2001/02/12 11:12    330  BC0THOR       *   FILE 558
//*        ENDVDATA   01.17  2002/01/16 17:12    525  BC0THOR       *   FILE 558
//*        ENDVFILE   01.04  2000/10/17 17:24    220  BC0THOR       *   FILE 558
//*        ENDVFLCK   01.08  2001/09/10 15:01    489  BC0THOR       *   FILE 558
//*        ENDVMTCH   01.04  1999/05/05 10:39     92  BC0THOR       *   FILE 558
//*        ENDVREFM   01.20  1999/05/05 10:40    188  BC0THOR       *   FILE 558
//*        ENDVSTRP   01.04  2000/06/12 17:30    304  BC0THOR       *   FILE 558
//*        ENQLIST    01.02  1999/08/31 15:14    682  BC0THOR       *   FILE 558
//*        EXCHANGE   01.16  2001/02/05 10:15    527  BC0THOR       *   FILE 558
//*        EXCPIO     01.71  2001/02/05 10:14   1143  BC0THOR       *   FILE 558
//*        EXCPSEQF   01.00  1989/09/26  9:54    546  USER02        *   FILE 558
//*        EXCPTAPE   01.06  1999/10/07 12:24    179  BC0THOR       *   FILE 558
//*        EXTSYMS    01.06  2002/02/22 11:26    193  BC0THOR       *   FILE 558
//*        FILES      01.17  1999/07/14 10:58    240  BC0THOR       *   FILE 558
//*        FINDCALL   01.04  2002/02/22 11:28    156  BC0THOR       *   FILE 558
//*        FINDCONT   01.03  2002/02/22 11:30    120  BC0THOR       *   FILE 558
//*        FINDDSN    01.01  1989/09/26  9:56    145  USER02        *   FILE 558
//*        FINDLDM    01.02  2002/02/22 11:33    438  BC0THOR       *   FILE 558
//*        FINDMAC    01.02  2002/03/26 13:38   2946  BC0THOR       *   FILE 558
//*        FINDPGM    01.00  2002/04/05 10:30    270  BC0THOR       *   FILE 558
//*        FINDSTRG   01.00  2002/02/22 11:36    452  BC0THOR       *   FILE 558
//*        FINDSUBR   01.02  2002/02/22 11:44    135  BC0THOR       *   FILE 558
//*        FNDALLMC   01.01  2000/08/02 14:45    655  BC0THOR       *   FILE 558
//*        FNDMACRO   01.10  2002/02/22 11:46    828  BC0THOR       *   FILE 558
//*        FREEPOOL   01.01  1995/09/26 16:24    135  BC0THOR       *   FILE 558
//*        GENDATES   01.00  2000/08/28 16:17    140  BC0THOR       *   FILE 558
//*        GENLDAT2   01.00  2001/12/07  9:09    421  BC0THOR       *   FILE 558
//*        GETDCB     01.01  1994/08/18 10:42    146  USER02        *   FILE 558
//*        GETDSNVL   01.05  1993/01/07  9:00    116  USER02        *   FILE 558
//*        GETGDG     01.03  1990/09/28  8:32     64  USER02        *   FILE 558
//*        GETOWNER   01.11  1993/12/08  9:04    289  USER02        *   FILE 558
//*        GETOWNR2   01.00  1993/12/08 10:36    182  USER02        *   FILE 558
//*        GETSMF     01.00  1989/09/26  9:57    241  USER02        *   FILE 558
//*        GETSYSID   01.01  2001/11/27  7:41     17  BC0THOR       *   FILE 558
//*        GETVOLS    01.04  1993/12/28  8:07     98  USER02        *   FILE 558
//*        GETVOLUM   01.04  1999/04/26 16:58     82  BC0THOR       *   FILE 558
//*        GETVSAM    01.00  1990/09/13 16:57    537  USER02        *   FILE 558
//*        GMABOVE    01.01  1996/01/04 15:59     66  BC0THOR       *   FILE 558
//*        GTRANDOM   01.04  1989/09/26  9:58    247  USER02        *   FILE 558
//*        HEX2ASKY   01.03  1999/08/31 15:28     66  BC0THOR       *   FILE 558
//*        HEX2PDEC   01.03  1989/09/26  9:58     54  USER02        *   FILE 558
//*        IEFSD095   01.00  2001/12/17  7:25    406  BC0THOR       *   FILE 558
//*        IEWBTEST   01.12  2002/01/31 17:54    584  BC0THOR       *   FILE 558
//*        IEWBUFF    01.03  2002/02/08 10:59      7  BC0THOR       *   FILE 558
//*        IEWBUFFE   01.04  2002/02/12  9:40     99  BC0THOR       *   FILE 558
//*        IEWBUFFM   01.01  2002/02/08 14:21     33  BC0THOR       *   FILE 558
//*        IEWBUFFN   01.02  2002/02/15 14:07     32  BC0THOR       *   FILE 558
//*        IEWBUFFP   01.01  2002/02/08 14:22     27  BC0THOR       *   FILE 558
//*        IEWBUFFR   01.02  2002/02/08 14:23     46  BC0THOR       *   FILE 558
//*        IEWBUFFS   01.01  2002/02/08 14:24     25  BC0THOR       *   FILE 558
//*        IEWBUFFT   01.01  2002/02/14  9:29     17  BC0THOR       *   FILE 558
//*        IEWBUFFX   01.01  2002/02/08 14:28     21  BC0THOR       *   FILE 558
//*        IEWBUFIB   01.01  2002/02/08 14:29     29  BC0THOR       *   FILE 558
//*        IEWBUFIL   01.01  2002/02/08 14:30     26  BC0THOR       *   FILE 558
//*        IEWBUFIU   01.02  2002/02/14  9:30     25  BC0THOR       *   FILE 558
//*        IEWBUFIZ   01.01  2002/02/08 14:32     24  BC0THOR       *   FILE 558
//*        IGGCSILC   01.01  2002/01/24 11:07    450  BC0THOR       *   FILE 558
//*        IGGCSI00   01.01  2002/01/24 11:04    362  BC0THOR       *   FILE 558
//*        ILBCHECK   01.15  1999/09/02 10:23    514  BC0THOR       *   FILE 558
//*        IL10STRP   01.00  2002/01/22 17:57    138  BC0THOR       *   FILE 558
//*        INQ500FE   01.00  2002/02/05 14:40     24  BC0THOR       *   FILE 558
//*        INVKSORT   01.00  1989/09/26  9:58    188  USER02        *   FILE 558
//*        IXVTOC     01.06  1993/06/02 11:31   1185  USER02        *   FILE 558
//*        JCLMODS    01.19  2001/04/27 10:23    724  BC0THOR       *   FILE 558
//*        JCLSCAN    01.05  2002/02/25  9:09    759  BC0THOR       *   FILE 558
//*        JCLSCAN2   01.13  2002/02/25  9:21    279  BC0THOR       *   FILE 558
//*        JOBINFO    01.03  1996/01/10 11:31     70  BC0THOR       *   FILE 558
//*        LDMDVER    01.03  2001/06/12 10:17    571  BC0THOR       *   FILE 558
//*        LIBPRNT    01.00  1989/09/26  9:59    129  USER02        *   FILE 558
//*        LISTPSWD   01.00  1989/09/26  9:59     70  USER02        *   FILE 558
//*        LISTVOLS   01.01  1998/12/18 15:33    193  BC0THOR       *   FILE 558
//*        LKEDANAL   01.06  2001/04/30 18:01    270  BC0THOR       *   FILE 558
//*        LKEDCTL2   01.04  1999/07/02 16:24    707  BC0THOR       *   FILE 558
//*        LKEDMODS   01.10  2001/05/31 17:39    795  BC0THOR       *   FILE 558
//*        LMODCHEK   01.09  2000/09/29 15:27    624  BC0THOR       *   FILE 558
//*        LMODHIST   01.03  2007/07/04 21:19    111  SBGOLOB       *   FILE 558
//*        LMODREAD   01.26  2002/02/12 15:17   1190  BC0THOR       *   FILE 558
//*        LOADDIR    01.00  1999/05/05 10:32    100  BC0THOR       *   FILE 558
//*        LOCDSNS    01.01  1989/09/26 10:00    259  USER02        *   FILE 558
//*        LOGREC     01.06  1999/01/15 17:09    298  BC0THOR       *   FILE 558
//*        LSTVTOC1   01.00  1989/09/26 10:00    246  USER02        *   FILE 558
//*        LSTVTOC2   01.00  1989/09/26 10:00    999  USER02        *   FILE 558
//*        LSTVTOC3   01.02  1993/07/29  9:51    410  USER02        *   FILE 558
//*        MACROEXP   01.02  2000/08/04 12:50     33  BC0THOR       *   FILE 558
//*        MERGE      01.01  1999/05/05 10:18    112  BC0THOR       *   FILE 558
//*        MERGE1A    01.06  1999/05/05 10:19    169  BC0THOR       *   FILE 558
//*        MERGE1B    01.01  1999/05/05 10:19    116  BC0THOR       *   FILE 558
//*        MERGE2     01.07  1999/05/05 10:19    166  BC0THOR       *   FILE 558
//*        MFCSIGNS   01.04  2000/05/12 16:25    244  BC0THOR       *   FILE 558
//*        MODINFO    01.02  2007/07/04 21:45    228  SBGOLOB       *   FILE 558
//*        MODPSWD    01.00  1989/09/26 10:01    126  USER02        *   FILE 558
//*        MODSCB     01.13  1989/09/26 10:01    253  USER02        *   FILE 558
//*        MODSCB2    01.06  1989/09/26 10:01    342  USER02        *   FILE 558
//*        MODSCNDY   01.01  2001/04/10 12:38    214  BC0THOR       *   FILE 558
//*        MODULENG   01.01  1999/05/05 10:32    117  BC0THOR       *   FILE 558
//*        MODXREF    01.02  2001/12/04 10:44   1061  BC0THOR       *   FILE 558
//*        MSASMRPT   01.00  2001/07/26 10:23    444  BC0THOR       *   FILE 558
//*        MSMCHMST   01.02  2001/07/24 10:33    151  BC0THOR       *   FILE 558
//*        MSMCHRPT   01.15  2001/07/25  7:34    459  BC0THOR       *   FILE 558
//*        MTCHMERG   01.09  1999/05/05 10:15     79  BC0THOR       *   FILE 558
//*        NOLIMIT    01.07  1993/03/01 13:33     21  USER02        *   FILE 558
//*        NUMERCHK   01.00  1998/07/06 16:27     41  BC0THOR       *   FILE 558
//*        OPCODE     01.14  2002/03/25 15:01    595  BC0THOR       *   FILE 558
//*        PARSEASM   01.04  2000/07/19 11:44    508  BC0THOR       *   FILE 558
//*        PDSCHECK   01.01  2001/04/24  9:19     96  BC0THOR       *   FILE 558
//*        PDSCLEAN   01.02  2001/06/16  1:45    467  BC0THOR       *   FILE 558
//*        PDSCPYMB   01.07  2002/02/25  9:28    100  BC0THOR       *   FILE 558
//*        PDSDIR     01.02  2001/09/05 17:07     50  BC0THOR       *   FILE 558
//*        PDSDIRB    01.16  1999/09/09 10:24    337  BC0THOR       *   FILE 558
//*        PDSDIRC    01.08  2001/05/31 12:34    261  BC0THOR       *   FILE 558
//*        PDSDIRLN   01.12  1998/09/23 15:50    210  BC0THOR       *   FILE 558
//*        PDSDSN     01.00  2001/05/16 11:42     87  BC0THOR       *   FILE 558
//*        PDSHIST    01.20  2007/07/04 14:15    154  SBGOLOB       *   FILE 558
//*        PDSINFO    01.06  2001/04/24  9:19    146  BC0THOR       *   FILE 558
//*        PDSREAD    01.18  2000/02/25  9:58    455  BC0THOR       *   FILE 558
//*        PDSVREPL   01.17  1998/08/11 13:52    298  BC0THOR       *   FILE 558
//*        PDSVUPDT   01.21  1998/09/04 11:06    679  BC0THOR       *   FILE 558
//*        PGMTYPE    01.00  1989/09/26 10:02    441  USER02        *   FILE 558
//*        PRINTDAE   01.03  2001/12/17 15:25    102  BC0THOR       *   FILE 558
//*        PRINTSUB   01.00  1989/09/26 10:02    120  USER02        *   FILE 558
//*        PRNTMULT   01.01  1989/09/20 10:06    209  USER02        *   FILE 558
//*        PROCSCAN   01.05  2002/02/25  9:50    312  BC0THOR       *   FILE 558
//*        PRTDSNH    01.00  1998/07/06 16:29    426  BC0THOR       *   FILE 558
//*        PRTPCH     01.01  2001/11/26 11:37    231  BC0THOR       *   FILE 558
//*        PULLDUPS   01.16  2001/11/26 10:53    254  BC0THOR       *   FILE 558
//*        PULLGRPS   01.08  2002/02/25 10:07    799  BC0THOR       *   FILE 558
//*        QSAMIO     01.18  2001/07/24 16:49    313  BC0THOR       *   FILE 558
//*        QWIKVTOC   01.01  1995/02/21 10:40    402  BC0THOR       *   FILE 558
//*        RANDOM     01.03  1989/09/26 10:03     22  USER02        *   FILE 558
//*        RCVRPDS    01.01  2002/04/02 14:33    464  BC0THOR       *   FILE 558
//*        RCVRVPDS   01.06  1990/08/17  9:44    464  USER02        *   FILE 558
//*        READDIR    01.04  2002/02/25 11:20    163  BC0THOR       *   FILE 558
//*        READFMEM   01.02  1989/09/26 10:04    137  USER02        *   FILE 558
//*        READLMOD   01.07  2002/04/02 16:25    413  BC0THOR       *   FILE 558
//*        READMEM    01.02  2002/02/25 11:20    167  BC0THOR       *   FILE 558
//*        READMEMX   01.00  1998/07/06 16:32    278  BC0THOR       *   FILE 558
//*        READVMEM   01.05  2002/02/25  9:51    139  BC0THOR       *   FILE 558
//*        REBUILD    01.48  2002/04/03  7:45   2686  BC0THOR       *   FILE 558
//*        RENSCR     01.00  1999/02/11 13:02    286  BC0THOR       *   FILE 558
//*        REQU       01.03  2002/01/21 14:40     22  BC0THOR       *   FILE 558
//*        RESCHECK   01.01  2002/03/18 13:58    206  BC0THOR       *   FILE 558
//*        RESOURCE   01.45  2002/04/02 16:44   1847  BC0THOR       *   FILE 558
//*        RMODE31    01.05  2000/08/03  8:44    127  BC0THOR       *   FILE 558
//*        SCANIMS    01.25  2000/07/25 12:59    201  BC0THOR       *   FILE 558
//*        SCANLDM2   01.06  1999/09/27 13:37    212  BC0THOR       *   FILE 558
//*        SCANLMOD   01.10  2002/02/11  7:13    165  BC0THOR       *   FILE 558
//*        SCANPSVB   01.09  1989/09/26 10:05    236  USER02        *   FILE 558
//*        SCANTEXT   01.02  2002/02/20 14:00    636  BC0THOR       *   FILE 558
//*        SCANTXT2   01.00  2001/04/17 11:34    639  BC0THOR       *   FILE 558
//*        SCANVBL2   01.11  1998/08/25 11:14    246  BC0THOR       *   FILE 558
//*        SCANVRBL   01.12  2002/02/25 10:33    304  BC0THOR       *   FILE 558
//*        SCANXREF   01.00  1998/07/06 16:34    476  BC0THOR       *   FILE 558
//*        SHUFFLE    01.01  1993/05/26 17:10     78  USER02        *   FILE 558
//*        SKELETON   01.02  2000/10/17 14:10    194  BC0THOR       *   FILE 558
//*        SMFABNDS   01.04  1998/10/30 13:18    341  BC0THOR       *   FILE 558
//*        SMFCOUNT   01.02  2002/01/19  9:47    434  BC0THOR       *   FILE 558
//*        SMFDSNAM   01.00  1999/09/20  8:30    768  BC0THOR       *   FILE 558
//*        SMFDSNM1   01.12  1999/09/20 14:33    305  BC0THOR       *   FILE 558
//*        SMFDSNM2   01.10  1999/04/12 13:10    463  BC0THOR       *   FILE 558
//*        SMFDSNV1   01.02  1999/11/17 13:52    349  BC0THOR       *   FILE 558
//*        SMFPRINT   01.00  1989/09/26 10:07    191  USER02        *   FILE 558
//*        SMFPRT30   01.00  1989/09/26 10:07    362  USER02        *   FILE 558
//*        SMFREAD    01.01  2002/01/19 14:25    466  BC0THOR       *   FILE 558
//*        SMFSTEPT   01.01  1998/10/31  9:18    332  BC0THOR       *   FILE 558
//*        SMFSTEP2   01.05  1994/04/15 14:49    153  USER02        *   FILE 558
//*        SMFSTEP3   01.02  1994/04/15 16:32    161  USER02        *   FILE 558
//*        SMFSTEP4   01.04  1994/04/18  8:58    200  USER02        *   FILE 558
//*        SMFSTRIP   01.08  1989/09/29 13:51    127  USER02        *   FILE 558
//*        SMFSTR14   01.25  1990/07/25 13:40    279  USER02        *   FILE 558
//*        SMFSTR30   01.26  1990/08/03 14:31    566  USER02        *   FILE 558
//*        SMFSTR64   01.02  1989/09/26 10:07    187  USER02        *   FILE 558
//*        SMFTSO     01.06  1989/09/26 10:08    348  USER02        *   FILE 558
//*        SQUEZE80   01.01  1989/09/26 10:08    178  USER02        *   FILE 558
//*        STAGE1IO   01.03  2002/01/16 17:12    220  BC0THOR       *   FILE 558
//*        STAGE2IO   01.03  2002/01/16 17:12    220  BC0THOR       *   FILE 558
//*        STIMER     01.00  1999/08/02 15:55     37  BC0THOR       *   FILE 558
//*        STORCREG   01.00  1989/09/26 10:09     46  USER02        *   FILE 558
//*        STRIP      01.11  2002/01/14 13:25    118  BC0THOR       *   FILE 558
//*        STRIPEDG   01.08  2002/01/14 12:25    457  BC0THOR       *   FILE 558
//*        STRIPLID   01.14  1990/09/27 12:07    203  USER02        *   FILE 558
//*        SVCDEXTR   01.00  1991/09/10 16:56    151  USER02        *   FILE 558
//*        SVCDMERG   01.08  1991/09/13 10:44    195  USER02        *   FILE 558
//*        SVCDREFM   01.00  1991/09/10 15:27    132  USER02        *   FILE 558
//*        SVCDREF1   01.13  1991/09/13 14:00    144  USER02        *   FILE 558
//*        SVCDREF2   01.09  1991/09/13 15:15    175  USER02        *   FILE 558
//*        SVLNK      01.00  1999/04/23 16:57     96  BC0THOR       *   FILE 558
//*        TAPEHEAD   01.07  1999/10/08 14:32    675  BC0THOR       *   FILE 558
//*        TAPESCAN   01.00  2001/01/05 11:40   1843  BC0THOR       *   FILE 558
//*        TCREPRT    01.04  2002/01/09  8:10    312  BC0THOR       *   FILE 558
//*        TGET       01.00  1999/05/21 16:16     65  BC0THOR       *   FILE 558
//*        TIME       01.00  1999/02/22 12:06    103  BC0THOR       *   FILE 558
//*        TIMECOMP   01.29  1999/01/14  9:13    285  BC0THOR       *   FILE 558
//*        TIMECONV   01.04  1999/01/15 13:47    116  BC0THOR       *   FILE 558
//*        TPUT       01.00  1999/05/21 16:16     62  BC0THOR       *   FILE 558
//*        TRACEDT    01.04  1993/08/06 12:16    269  USER02        *   FILE 558
//*        TRACEOFF   01.04  2001/07/25 14:06     38  BC0THOR       *   FILE 558
//*        TRACEON    01.06  2001/07/25 14:07    306  BC0THOR       *   FILE 558
//*        TSODUMP    01.00  1989/09/26 10:10    793  USER02        *   FILE 558
//*        UCB        01.00  1989/09/26 10:10     31  USER02        *   FILE 558
//*        UCBLKUP    01.01  1989/09/26 10:10    312  USER02        *   FILE 558
//*        UCBLOOK    01.00  2001/02/05  9:44     27  BC0THOR       *   FILE 558
//*        UCBREPRT   01.00  1989/09/26 10:10    197  USER02        *   FILE 558
//*        UCBSCAN    01.01  1999/04/28 16:37    167  BC0THOR       *   FILE 558
//*        UCBSRCH    01.01  1989/09/26 10:10     46  USER02        *   FILE 558
//*        UNIQUE     01.04  2001/09/12 15:30    292  BC0THOR       *   FILE 558
//*        UNSQUZ80   01.01  1989/09/26 10:10    188  USER02        *   FILE 558
//*        UPDMEM     01.09  2000/10/10  9:55    188  BC0THOR       *   FILE 558
//*        UPDTLMOD   01.02  1992/07/09 13:33    177  USER02        *   FILE 558
//*        USECPU     01.13  1990/08/27 10:24    116  USER02        *   FILE 558
//*        USERABND   01.03  2000/06/04 10:34    100  BC0THOR       *   FILE 558
//*        VBSCHECK   01.02  1992/05/19 10:36    143  USER02        *   FILE 558
//*        VERCSECT   01.01  1990/03/06 17:08    518  USER02        *   FILE 558
//*        VERLDMOD   01.08  1990/03/06 10:11    739  USER02        *   FILE 558
//*        VOLFILE    01.09  1998/12/28 19:16    219  BC0THOR       *   FILE 558
//*        VOLLIST2   01.19  1994/03/30 15:47    339  USER02        *   FILE 558
//*        VOLSPACE   01.00  1999/04/01 16:24    344  BC0THOR       *   FILE 558
//*        VOLSPOLD   01.00  1993/11/18 10:33    353  USER02        *   FILE 558
//*        VRNDUPDT   01.01  1990/02/16 11:04    399  USER02        *   FILE 558
//*        VSAMFILE   01.04  2000/10/17 17:09    265  BC0THOR       *   FILE 558
//*        VSAMHIST   01.01  1993/11/17 12:00    533  USER02        *   FILE 558
//*        VTOCDATA   01.03  1991/10/31 15:53    368  USER02        *   FILE 558
//*        VTOCDSVL   01.00  1999/10/01 11:39    132  BC0THOR       *   FILE 558
//*        VTOCLISG   01.06  1991/07/02 13:33    658  T7895         *   FILE 558
//*        VTOCLIST   01.00  1989/09/26 10:12    353  USER02        *   FILE 558
//*        VTOCPRNT   01.03  1991/11/01 10:46    133  USER02        *   FILE 558
//*        VTOCSTRP   01.05  1989/09/26 10:12    220  USER02        *   FILE 558
//*        WAITASEC   01.00  2002/02/11 11:33     65  BC0THOR       *   FILE 558
//*        WAIT5MIN   01.01  1990/06/18 11:06     35  USER02        *   FILE 558
//*        WHERE      01.16  2001/07/13 13:26    825  BC0THOR       *   FILE 558
//*        WHEREAMI   01.02  2001/11/08 13:04     31  BC0THOR       *   FILE 558
//*        WRITEKL    01.02  2000/10/25 10:46    100  BC0THOR       *   FILE 558
//*        WTOEXP     01.06  1989/09/26 10:12     26  USER02        *   FILE 558
//*        WTOEXP1    01.01  1999/11/11 11:33     28  BC0THOR       *   FILE 558
//*        WTOHI      01.01  2001/04/23 15:11     68  BC0THOR       *   FILE 558
//*        WTOLO      01.02  2001/04/23 13:45     79  BC0THOR       *   FILE 558
//*        WTOPGMR    01.02  2001/04/24  8:17     79  BC0THOR       *   FILE 558
//*        WTOREGS    01.06  1996/04/04 15:44     75  BC0THOR       *   FILE 558
//*        WTORTEST   01.02  1999/11/08 14:23     28  BC0THOR       *   FILE 558
//*        XMEM       01.17  1990/11/28 10:11    209  USER02        *   FILE 558
//*        XMEMGET    01.00  1989/09/26 10:13    358  USER02        *   FILE 558
//*        XMEMTEST   01.00  1989/09/26 10:13    281  USER02        *   FILE 558
//*        XPRNT      01.01  1995/02/03 15:45     21  BC0THOR       *   FILE 558
//*        XREAD      01.00  1995/02/03 15:31     28  BC0THOR       *   FILE 558
//*        XWHERE     01.03  1990/11/20 14:38    306  USER02        *   FILE 558
//*                                                                 *   FILE 558
```
