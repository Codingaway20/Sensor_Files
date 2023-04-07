/*****************************************************************************************
 * Copyright (c) 2017, Nicolás Boettcher
 * All rights reserved.
 *
 * Redistribution and use in source and binary forms, with or without modification, are 
 * permitted provided that the following conditions are met:
 *
 *    * Redistributions of source code must retain the above copyright notice, this list  
 * of conditions and the following disclaimer.
 *    * Redistributions in binary form must reproduce the above copyright notice, this  
 * list of conditions and the following disclaimer in the documentation and/or other 
 * materials provided with the distribution.
 *    * Neither the name of Nicolás Boettcher nor the names of its 
 * contributors may be used to endorse or promote products derived from this software 
 * without specific prior written permission.
 *
 * THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY 
 * EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF 
 * MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL 
 * THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, 
 * SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, 
 * PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS 
 * INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, 
 * STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF
 * THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 *
 * - Revision -------------------------------------------------------------
 * $Revision: 1.0 $
 * $Date: 2017/03/03 $
 * @author: Nicolás Boettcher @nicoboettcher
*****************************************************************************************/

The following folders contain the ContikiOS 3.0 platform definition for Advanticsys new platform, 
the XM1000.

Installation Guide:

==========================================================================================
ASSUMPTIONS
==========================================================================================

A. This guide assumes you have a running ContikiOS installation, which at this moment is 
Contiki 3.0. If that is not the case, first of all install ContikiOS following the instruc-
tions in ContikiOS github:

git clone https://github.com/contiki-os/contiki.git

==========================================================================================
PLATFORM INSTALLATION
========================================================================================== 

To add support for this platform to an existing ContikiOS installation, follow these steps:

Now we need to add xm1000 compatibility to our contiki.

Thanks to DMI (https://www.blogger.com/profile/05933386863009488617) for the xm1000 patch. 
Without it, you will see the following error:

make: *** No rule to make target 'obj_xm1000/cc2420.o', needed by 'contiki-xm1000.a'.  Stop.

I upgrade his patch with an app to access to the xm1000 sensors.

Now, extract both folders ('platform' and 'tools') into your contiki folder.

Go to the apps folder and execute an script that I create to automate the process:

cd $YOUR_CONTIKI_PATH/platform/xm1000/apps/sensors
./install.sh

Enjoy it!

