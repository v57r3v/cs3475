java c
Introduction to   Digital   Logic   Design   Lab
EECS   112L
1            Install   The   Vivado   Design   Suite
Vivado is a software produced by Xilinx for synthesis   and   analysis of HDL   designs.    The WebPack version   of Vivado   is   free   and   You   can   download   and   install   it   from   here:
https://www.xilinx.com/support/download.html
1.1            Download   the   Vivado   Design   SuiteSelect the   appropriate version for your   laptop   operating   system.    There is   no   oﬃcial   Vivado   for   the   Mac.   If   you      are   using   Mac   you   need   to   install   Vivado   on      a   virtual   machine   or   use   Vivado   on   one   of   UCI   servers.
•   Vivado   on   Windows
–      Example:   Choose ” Xilinx Uniﬁed Installer 2020.2:   Windows Self   Extracting Web Installer” to   download the Vivado   Design   Suite   for Windows   machine.    (This   is the   latest   version   available   but   all   2017,   2018,   and   2019   versions   are   ok)
•   Vivado   on   Linux
–      Choose   ”Xilinx   Uniﬁed   Installer   2020.2:    Linux    Self   Extracting   Web   Installer”   to   download   the   Vivado   Design   Suite   2020.2   for   Linux   machine.
•   Vivado   on   Mac
–      Run   Windows   or   Linux   on   a   Virtual   Machine
*      Download   either   Windows   or   Linux   web   Installer
–      Use   Vivado   on   EECS   server.    The   current   version   on   the   EECS   server   is   2017.1   which   is   ok   for   the   purpose   of this   course
   You need a Xilinx account to   download   the   tool.    Register with   your   UCI   net   ID   and   sign   in   to   download   the   Xilinx   toolchain.    This   would   be   a   ﬁle   around   248MB   (for   windows)   which   will   both   download   and   install   the   tool   for   you.
   
1.2            Install   the   Vivado   Design   Suite
This   section   explains   the   installation   process   for   all   platforms   for   the   Vivado   Design   Suite.   Couple   points   before   extracting   and   installing   the   tool:
•      Make   sure   your   machine   can   support   this   toolchain.   You   can   check   this   on   Xilinx   website.
•      Make   sure   that   you   have   enough   space   on   your   system   for   this   tool.      It   might   take   up   to   a   few   Gigabytes
Now,   let’s   start   the   installer   you   have   downloaded   in   the   previous   step.      After   you   click   on   the   installer   it   will   extract   the   tool   and   prepare   it   for   the   installation.

To install Vivado on Linux:• Open a terminal and run:$chmod +x Xilinx Unified 2020.2 1118 1232 Lin64.bin$sudo ./Xilinx Unified 2020.2 1118 1232 Lin64.bin• Vivado Installer window will appear. The instalation process is same as windows.• After installing Vivado, open a terminal and type these two commands to run thesoftware :$source /opt/Xilinx/Vivado/2020.2/settings64.sh$vivado


Click   Next.
   A   window   will   pop   up   asking   about   your   installation   type   and   your   Xilinx   account.    You   can   use   the      account   you   have   made   at   the   beginning   on   the   Xilinx   website.    Select   the   ”download   and   install   now”   option.      Click   Next.
   
1.3            License   and   Edition   Selection
In the   next   step,   you would   select which   edition   of the Vivado   tool   you   want   to   install.    For   now,   we   can   install   the   webpack   version   which   doesnt   require   any   license.
This   window   asks   you   about   the   tool   you   want   to   install.      Select   Vivado   and   click   Next.
   
We   are   going   to   use   the   free   version   so,   here   select   ”Vivado   HL   WebPack”   .
   
Here   the   default   options   are   ok.      Click   Next.
   
Accept   the   licencse   agreement   and   selest   all   ”I   Agree”   boxes.
   
Select   the   installation   directory.      Click   Next.
   
Click   Install.
   
1.4            Download   and   installationThe   ﬁnal   section   of the   installation   will   start   to   download   the   full   image   of the   Vivado   tool   which   even   with   a   fast   internet   connection   will   take   quite   a   long   time.    Try   to   do   this   part   before   the   class.    After   downloading   the   full   image   the   installation   process   will   begin.


   

Use the Vivado software on the EECS server:Note : The mo代 写EECS 112L Introduction to Digital Logic Design LabHaskell
代做程序编程语言st updated version Vivado on the server is 2017.1 which is still enough forthis course.• Connect to one of the Servers– zuma.eecs.uci.edu– laguna.eecs.uci.edu– crystalcove.eecs.uci.edu– bondi.eecs.uci.edu• Open a terminal and loging with your username$ssh -X -Y UserName@ServerName• Type this command in the terminal to setup Vivado 2017.1$source /ecelib/eceware/xilinx/Vivado/2017.1/settings64.csh• Type vivado to lunch the application$vivado


2            Using   The   Vivado   Design   Suite
Open   Vivado   from   your   desktop.


Select   Create   Project.
   
Click   next.
   Your   new   project   needs      a   name,      an      address    (location   on   your   computer),      and      a   collection   of   design   source   codes.    This   new   window   asks   you   to   choose   a   name   for   your   project,   and   specify   the   directory   that   you   want   to   save   your   project   in.
   Vivado Naming Conventions:Project names and source file names must start with a letter (A − Z, a − z) andmust contain only alphanumeric characters (A-Z, a-z, 0-9) and underscores( ).
This   new   window   asks   you   to   determine   the   type   of your   project.    Select   ”RTL   Project”   in   the   Project   Type   form.      Select   ”Do   not   specify   sources   at   this   time”   (we   will   talk   about   this   later).      Click   Next.
   Note:You can define different types of projects in Vivado.• RTL Project - RTL to Hardware Validation– Import RTL and IP to process design all the way to hardware– Standalone IP - Create reusable preconfigured IP module– Device exploration - Empty project to examine device resources• Post-synthesis Project Netlist to Hardware Validation– Third Party synthesis• I/O Planning Project Early I/O Exploration and Assignment– Create I/O port manually or import CSV, RTL, or XDC– Can migrate to RTL Project• Imported Project - Migrate Project from Synplify, XST, or ISE Project– Imports sources and compilation order– No synthesis or implementation result imported– No tool setting migrated• Example project– Using Vivado examplesIn the   Default   Part   dialog   box,   you   should   select the   family   and   part   number   of the   FPGA you want   to   implement   your   code   on.      Since   in   this   course   we   are   not   going   to   work   with   any   FPGAs,   you   may   skip   this   step   and   click   Next.
   
Review   the   project   summary   in   the   New   Project   Summary   dialog   box   before   clicking   Finish   to   create   the   project.
   You   see   diferent   windows   in   the   Vivado   software:   Flow   Navigator,   Sources,   Project   summary,   and   etc..
   
The   Project   summary   will   give   you   the   status   of your   project.
Throughout   this   course   we   are   going   to   use   Verilog   language   (or   System   Verilog)   for   hardware   design.   We   can   change   the   target   language   by   going   to   the   Project   Summary   window   and   click   Edit.   
2.1            Design   a   Half Adder
We   want   to   design   a   Half Adder.   You   see   the   block   diagram   below.From the Flow Navigator window, choose Add Sources.    Select ”Add or create design sources”   , click Next.
   
We   want   to   create   a   new   ﬁle   so,   click   ”Create   File”   .
   
Deﬁne   a   name   for   your   design.      Click   Ok   and   Finish.
   
The   next   window   asks   you   to   deﬁne   I/O   ports   for   your   module.      We   are   going   to   deﬁne   them   later   in   the   code   so   skip   this   part   and   click   Ok.
   
Now   you   see   your   new   source   ﬁle   (HA)   under   Design   Sources   in   the   Sources   window.
   
Double   click   on   HA   to   open   it.
   
Below   you   see   the   Verilog   code   for   a   Half Adder.    Copy   and   paste   this   code   to   the   HA.v   window.   Code   1:      Half Adder.
module   HA
(
A   ,
B   ,
Sum   ,
Carry
)   ;
input
input
output
output
assign
assign
A   ;
B   ;
Sum   ;
Carry   ;
Sum            =   A         B   ;         //   bitwise   xor
Carry         =   A      B   ;         //   bitwise   and
endmodule   //   half_adder
If   you   have   a   syntax   error   in   this   part,   the   line   which   contains   error   will   be   underlined   by   red   color.   Make   sure   to   correct   all   of them.    Save   your   code.
   



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
