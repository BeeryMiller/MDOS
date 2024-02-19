There are GIT utilities for Windows and I am sure other platforms as well to retrieve a repository.  The source files will be Text files (not D/V 80), so drag them over to a TIPI folder.  Make sure in the PI.CONFIG file, you have the root directory (I use MDOS) set as NATIVE_TEXT_DIRS=MDOS.
 
This will insure the PI treats the PC text files as DIS/VAR 80 files for assembly.

You can not link the OBJect files on the TIPI due to a TIPI PAB limitation that limits file sizes to 64K and we are at 140K for the binary image.  So, copy the files to a HRD, IDE, SCS, or HDS device.  When you copy them over, they will copy/convert over as DIS/VAR 80 files as long as you have the NATIVE_TEXT_DIRS=directory-name properly set.

From there, as long as you have the GenPROG tools (ASM, $MAKE, LINK) in a path (they are in the TOOLS directory if you do not have them), you can type MAKE in the directory where you have copied the files too, and you can then assemble the files.  All OBJect files will be saved to an OBJ folder so make sure you have created the OBJ subfolder.  The MDOS image will be in the BIN folder called MDOS.
