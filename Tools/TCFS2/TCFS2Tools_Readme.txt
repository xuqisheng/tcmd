TCFS2Tools Module for Total Commander
-------------------------------------
(English section is below)

��������� ���������������� ������� TCFS2, ��������:
+ ��������/���������� ������ �������� ����
+ �������� ���������� ������� ���� ��������� ��� ������
+ ���������� ������� ���� � ���� ������������ �� ������� ������������
+ ��������/������������� ������� ����������� �������� �������
+ �������� ������� ������ �������
+ �������� ��������� ��������, ������������ �������� GetSystemMetrics
+ �������� ������� ������� ������� ������



1. ���� ������������ � �������� ������

���������������� ���� ������ ���������� � ����� ������ � ����� ����� �� ��� �����, �� ���������� INI. ���� ������������ ���������, ������ ���� ����� �������������� ����������� �������������� ������ � ����� (������� ���� ����� ������ ���������). ������� ������� �� 2 ���� - TCM (� �������� ���������������) � STR (�� ��������� ���������������). ��� �������� �� � ������, ������� � ������� 2 ������� �����.

��������� ������ [HideMenu]:
	MenuMode=0
		������ ����� ����������� �������� ���� ��� ������, ����� ��� ������: 0 - ��� ������� Alt ������� ���� �������� ����������; 1 - ��� ������� Alt ������� ���� ������������ � ���� ������������.

������� ������ [HideMenu]:
	ShowMainMenu=65537
		���������� ������ ���� (���� ��� ���� ������);
	HideMainMenu=65538
		�������� ������ ����;
	SwitchMainMenu=65539
		����������� ��������� ������ ����;
	TrackMainMenu=65540
		���������� ������� ���� � ���� ������������ ����.

������� ������ [Common]:
	GetWindowMetrics=65550
		���������� ������� � ��������� ���� ��. �������� lParam ����������, ����� ������ �������� ������������: 0, 1, 2, 3 - ���������� X, Y, ������ � ������ ����; 4, 5, 6, 7 - ���������� X, Y, ������ � ������ ���������� ����� ���� (��� ���������, ���� � ������);
	LeftIsActive=65551
		���������, ������� �� ����� (�������) ������, � ���������� 1 ��� 0;
	RightIsActive=65552
		���������, ������� �� ������ (������) ������, � ���������� 1 ��� 0;
	LeftGetViewMode=65553
		���������� ������ ���������� ������� �� ��� ������������ ����� ������ � ������� ����� (101 - �������, 102 - ���������, 71 - ������ ���������������� � �.�.). �������� ������ ��� �������, ��������� � ���� �� cm_LeftCustomViewMenu;
	RightGetViewMode=65554
		�� ��, ��� � LeftGetViewMode, �� ��� ������ ������;
	IsVerticalPanels=65555
		���������� 1, ���� ������ ������������ ���� ��� ������;
	GetPanel=65556
		���������� ���������� ���� ������ ��. �������� lParam ���������� ������: 1 - �����, 2 - ������;
	SeparatorGet=65561
		���������� ������� ����������� �������� �������;
	SeparatorSet=65562
		������������� ������� ����������� �������, ���������� � lParam. ���� �������� ������ ����, ������� ���������� ����� ����� ���������� �����;
	LeftTabIndex=65580
		���������� ������ ������� ������� ����� (�������) ������;
	RightTabIndex=65581
		���������� ������ ������� ������� ������ (������) ������;
	LeftTabCount=65582
		���������� ����� ������� �� ����� (�������) ������;
	RightTabCount=65583
		���������� ����� ������� �� ������ (������) ������;
	LeftTabSetIndex=65584
		���������� �� ����� (�������) ������ ������� � ��������, ���������� � lParam;
	RightTabSetIndex=65585
		�� ��, ��� � LeftTabSetIndex, �� ��� ������ ������;
	LeftTabIsLocked=65586
		���������� ���������� � ����������������� ������� ����� (�������) ������: 9 - �������������, 11 - ������������� � ������������ ����� ��������, 0 - �� �������������. �������� lParam ����� ����� ������� (������� � 1), 0 - ��� ��������;
	RightTabIsLocked=65587
		�� ��, ��� � LeftTabIsLocked, �� ��� ������ ������.

������� ������ [System]:
	GetSystemMetrics=65570
		���������� �������� ��������� ��������� �������� � ��������, ���������� � ��������� lParam. �������� �������������� �������� �������� � �������� ������� GetSystemMetrics (��������, 0 - ������ ��������� ������, 1 - ������ ��������� ������, 4 - ������ ��������� ����) - �������� ����� 50 ��������;
	GetWorkArea=65571
		���������� ������� � ������������ ������� ������� ������ (��� ������ �����). �������� ��������� lParam ����������, ����� ������ �������� ����� ������� (0 - ������, 1 - ������, 2 - �������������� �������, 3 - ������������ �������);
	GetAsyncKeyState=65572
		���������� ���������� � ��������� �������. �������� lParam ������ ����������� ��� �������. ���� ������ � ������������ �������� �������� � �������� ������� GetAsyncKeyState (��������, 16 - Shift, 17 - Ctrl, 18 - Alt; ������������� ��������� ��������, ��� ������� ������);
	GetSomeInfo=65573
		���������� ��������� ���������� � ����������� �� �������� lParam: 0 - ���������� ����������� � ������� �������� Windows.

������� ������ [Registers]:
	RegWrite=RegWrite
		���������� �������� � ���� �� ���������. ���������: wParam - ����� �������� (������� � 1), lParam - �������� ��� ������;
	RegRead=RegRead
		��������� �������� �� ��������. ���������: wParam - ����� ��������, lParam - ��������, ������������ ��� ������;
	RegCount=RegCount
		���������� ���������� ��������� ��������� (��������� � ������������ ������� ��������).

���������������� ������ TCM-������ �� ������ ��������� � �������� ������ �� (������ ������������ � �� ������� ����� ���������� � ����� TOTALCMD.inc).

��� ����������� ��������� �� ��������� ��������������� ��� �������� ��������� "TCFS2." (��������, TCFS2.RegRead), ���� ���� ������������� ���������������� - ��� �������� ��������� ����� ���������� ��������� ��� ���������.



2. ����� ������

2.1 ����� TCM-������

��� ������ �����-���� ������� ����� ��������� ������� ��������� � ������� WM_USER+51 ($433) ���� �� ��� ����������� ������ TCFS2Tools. ������ ���������� ��������� � ������ ���������. � �������� ��������� wParam ��������� ����� ������� ����� ������� TCFS2Tools (������� � ������� 1 ������� �����). ���� ������� ��������� ��������, ��� ����� ��������� � �������� ��������� lParam ���������.

���� ������ �� ��������, �� ��������� ������� ��� ���������� � ���������� � ���������. ��� ���� � ����������� ������� �������� ���������, ��� ������� �� ����������� (���������� ������� �� ����� ������ �������).


2.2 ����� ������ �� ���������� ����������������

��� ������ ������� ���������� �������� ����� �������� ��������� � ������� ������� RegisterWindowMessage, ������ ������������� ��������� � ���������� "TCFS2." (��������, TCFS2.RegRead). ���� ������� ��������� ���������, �� ����� ��������� � �������� ���������� wParam � lParam ���������.

���� ������ �� ��������, ��������� �� ����� ����������.



3. ���������� � TCFS2

����� TCFS2 (�������� �������� �����: http://wincmd.ru/plugring/tcfs2.html) ��������� ��������� �������� ���� ��, � ��� ����� � �������� ���������� ������� ��. ����� ��������� ������� TCFS2Tools ��� ����������, ����� ������������ ������� tcm, ��� ���������� ������� � ���������� - ������� msg. � �����, tcm(x) �������� ��� msg($433, x, 0, 0). ��� ������������� ������������ TCFS2Tools �������� ��������� ������� � ������ [Items] ����� ������������ TCFS2:

mm1=tcm(65537)
mm0=tcm(65538)
mm2=tcm(65539)
mm_track=tcm(65540)
set_separator=msg($433, 65562, #1)
regwrite=msg(regmsg(TCFS2.RegWrite), #1, #2)
...

�������, ������������ ��������, ����� ������������ � �������� ������ ��������. ����� � TCFS2 � ������ 2.0 ����� ��������� �� � ������ [Macros] � �������� �� ���������� �������:

sepPos=msg($433, 65561)
L_isActive=tcm(65551)
L_viewMode=tcm(65553)
cxScreen=msg($433, 65570, 0)
cxWorkArea=msg($433, 65571, 0)
pressedShift=msg($433, 65572, $10) < 0
regread=msg(regmsg(TCFS2.RegRead), #1, #2-0)
...

����������, ������ ������ ��� �������������� ��������� ������ ��������� � ���������� � ����� ������������ TCFS2Tools, ���� �� �� ���������������. � ����������� ����� ������������ TCFS2 ��� ��������� ��������� �������, ������������ TCFS2Tools. ��� �������� ��������� �� ��������� ��������������� ���������� TCFS2 ������ 2.0.4 � ����.



4. �������� ��� ������� ��

���� ������� 2 ������� �������� ������ ��� ������� ��. ������ ������ ����������� � ����������� TCFS2Tools.dll � �������� WDX-������ �� � ����������� ������������ ������������ ������� ����� ��� ����� ������ (������������, �����, ��� ����� ������, ��������, ������, ������� �������, "TCFSTools.Autorun > 0", ��������� � ����� ������, ������� ����� ����, ��������� ��� ���������), ������������� �� ��������� ������ �������������.

�� ����� ������ ������������ ���������� ������ ����������� Autorun.wdx, ����� ���������� ��������� � ��� Autorun.cfg ��������� ������:

LoadLibrary "X:\Path\To\TCFS2Tools.dll"


���������� �� ����������� ������������� ������: http://forum.wincmd.ru/viewtopic.php?t=13332



TCFS2Tools Module for Total Commander
-------------------------------------
(English section)

Expands TCFS2 functionality by allowing to:
+ show/hide main menu
+ temporary show main menu on menu call
+ show main menu as popup menu on user command
+ get/set file panel separator
+ get current view modes for panels
+ get system metrics via function GetSystemMetrics
+ get width and height of desktop work area



1. Configuration file and commands description

Configuration file should be placed near module and have same name and extension INI. You need it only if you wish to redefine default command identifiers and options (specified below after equals signs). There are two command types - TCM (with numeric id) and STR (with literal id). Read section 2 of this file to know how to call both.

Parameters for [HideMenu] section:
	MenuMode=0
		Main menu display mode when it is hidden: 0 - when Alt is pressed, main menu is temporary enabled; 1 - when Alt is pressed, main menu is displayed as popup menu.

Commands for [HideMenu] section:
	ShowMainMenu=65537
		Show main menu;
	HideMainMenu=65538
		Hide main menu;
	SwitchMainMenu=65539
		Switch main menu;
	TrackMainMenu=65540
		Display main menu as popup menu.

Commands for [Common] section:
	GetWindowMetrics=65550
		Gets TC window dimensions and position. Parameter lParam specifies what to retrieve: 0, 1, 2, 3 - coordinates X, Y, width and height of entire window; 4, 5, 6, 7 - coordinates X, Y, width and height of client part of window (w/o title, menu and borders);
	LeftIsActive=65551
		Checks if left (top) panel is active and returns 1 or 0;
	RightIsActive=65552
		Checks if right (bottom) panel is active and returns 1 or 0.
	LeftGetViewMode=65553
		Gets internal command index of current view mode for left panel (101 - brief, 102 - full, 71 - first custom mode etc.). Works only for modes listed in menu on cm_LeftCustomViewMenu;
	RightGetViewMode=65554
		Like LeftGetViewMode but for right panel;
	IsVerticalPanels=65555
		Checks if vertical panels arrangement is enabled and returns 1 or 0;
	GetPanel=65556
		Gets TC panel handle. Parameter lParam specifies panel: 1 - left, 2 - right;
	SeparatorGet=65561
		Gets file panels separator position;
	SeparatorSet=65562
		Sets file panels separator position. You must pass new position in lParam parameter. If parameter is less than zero mouse will be used to move separator;
	LeftTabIndex=65580
		Gets active tab index for left (top) panel;
	RightTabIndex=65581
		Gets active tab index for right (bottom) panel;
	LeftTabCount=65582
		Gets tabs count for left (top) panel;
	RightTabCount=65583
		Gets tabs count for right (bottom) panel;
	LeftTabSetIndex=65584
		Activates tab with index passed in lParam for left (top) panel;
	RightTabSetIndex=65585
		Like LeftTabSetIndex but for right panel.
	LeftTabIsLocked=65586
		Gets left (top) panel's tab locked state: 9 - locked, 11 - locked with directory changes allowed, 0 - not locked. Parameter lParam specifies 1-based tab index, 0 means active tab;
	RightTabIsLocked=65587
		Like LeftTabIsLocked but for right panel.

Commands for [System] section:
	GetSystemMetrics=65570
		Gets system parameter value depending on index passed in lParam. Refer to GetSystemMetrics function documentation for supported indexes (e.g. 0 - primary screen width, 1 - primary screen height, 4 - window caption height) - there are more than 50 values;
	GetWorkArea=65571
		Gets desktop work area dimensions and position (w/o taskbar). Parameter lParam specifies which value you need to return (0 - width, 1 - height, 2 - horizontal position, 3 - vertical position);
	GetAsyncKeyState=65572
		Gets information about key state. Parameter lParam specifies virtual-key code. Refer to GetAsyncKeyState function documentation for virtual-key codes and return value description (e.g. 16 - Shift, 17 - Ctrl, 18 - Alt; negative return value tells that key is pressed);
	GetSomeInfo=65573
		Gets some information depending on lParam value: 0 - number of msecs since Windows start.

Commands for [Registers] section:
	RegWrite=RegWrite
		Stores a number in a cell. Parameters: wParam - cell address (starting from 1), lParam - value to store;
	RegRead=RegRead
		Reads a value from a cell. Parameters: wParam - cell address, lParam - value that is returned on error;
	RegCount=RegCount
		Returns number of available cells (same as last cell address).

You must choose numbers not used by TC if you redefine command indexes (read TOTALCMD.inc file for used numbers).

Module adds "TCFS2." prefix to all literal ids that it registers (e.g. TCFS2.RegRead) even if you redefine it - when you send a message, you should add this prefix too.



2. Commands execution

2.1 TCM-commands

In order to call some command you need to send message with number WM_USER+51 ($433) to TC window after loading TCFS2Tools. Module will process message and return result. You need to specify command index as wParam message parameter. If you call command with parameter, you must pass it in lParam parameter.

If you don't have TCFS2Tools loaded or installed, TC will try to execute command itself. In most of cases it will show message that function is not realized (internal TC commands have another indexes).

2.2 STR-commands

You should get window message number associated with literal id using function RegisterWindowMessage. Don't forget to specify identifier with "TCFS2." prefix (e.g. TCFS2.RegRead). If command accepts parameters, you should pass them via wParam and lParam message parameters.

If TCFS2Tools is not loaded, message won't be processed.



3. Integration with TCFS2

TCFS2 Addon (download page is here: http://www.totalcmd.net/plugring/tcfs2.html) allows to control TC window modes, including sending TC internal commands. You should use tcm command in order to call TCFS2Tools command w/o parameters or msg command if you need to pass some parameters. By the way, tcm(x) acts like msg($433, x, 0, 0). You may add following lines to [Items] section of TCFS2 configuration file:

mm1=tcm(65537)
mm0=tcm(65538)
mm2=tcm(65539)
mm_track=tcm(65540)
set_separator=msg($433, 65562, #1)
regwrite=msg(regmsg(TCFS2.RegWrite), #1, #2)
...

Commands that return values may be used as check commands. Also since TCFS2 2.0 you may add some values to [Macros] section and call directly from parameters of functions:

sepPos=msg($433, 65561)
L_isActive=tcm(65551)
L_viewMode=tcm(65553)
cxScreen=msg($433, 65570, 0)
cxWorkArea=msg($433, 65571, 0)
pressedShift=msg($433, 65572, $10) < 0
regread=msg(regmsg(TCFS2.RegRead), #1, #2-0)
...

Of course, command indexes or literal identifiers must be the same with ones in HideMenu configuration file if you've redefined them. Default TCFS2 configuration file already has some commands that use TCFS2Tools. You need TCFS2 version 2.0.4 to be able to send messages with literal ids.



4. Loading module on TC start

There are at least two ways to load module on TC start. First way is to register TCFS2Tools.dll as WDX plugin and to define special 'color by file type' preset (Configuration, Color, by file type, Add, Define, Plugins tab, "TCFSTools.Autorun > 0", save with any name, select any color, apply all changes) to cause TC to load TCFS2Tools automatically.

You may also use Autorun.wdx content plugin in order to load HideMenu module on TC start. You need to add following line to Autorun.cfg file:

LoadLibrary "X:\Path\To\TCFS2Tools.dll"


Discussion page on official board: http://www.ghisler.ch/board/viewtopic.php?t=29700



History:

2016-02-01	1.4.4.216
	* active panel detection after closing FTP connection

2015-02-22	1.4.4.214
	+ some commands to get information about tabs and set active tab
	* FTP connect/disconnect could return hidden main menu back, and then Alt could destroy menu on hiding
	* WM_INITMENUPOPUP is not suppressed anymore when main menu is hidden
	* fixed returning hidden main menu back by WM_INITMENUPOPUP

2014-02-10	1.4.3.188
	+ GetPanel command to get panel window handles

2013-07-09	1.4.3.180
	+ GetWorkArea is now able to return also work area position
	+ workaround for idle menu items in 64-bit version when menu is hidden (Lazarus thing)
	+ adjust popup menu dimensions in 64-bit version
	* wrong work area size returned in case of left or top taskbar position

2012-11-17	1.4.2.158
	+ command to check vertical panels arrangement
	+ get/set separator commands now work with vertical panels

2011-11-14	1.4.2.130
	+ 64-bit version of module added
	+ commands to write numbers to internal array and read them back

2011-09-10	1.4.1.114
	+ commands to get exact current view mode for TC panels
	+ command to get TC window dimensions
	+ command to get some system information like number of msecs since Windows start

2011-05-07	1.4.0.88
	+ may be loaded w/o Autorun.wdx
	+ commands to get/set separator pos
	+ command to get work area width and height (w/o taskbar)
	+ command to get any GetSystemMetrics value
	+ command to get any key state

2010-11-20	1.2
	+ commands to check if left/right panel is active

2010-06-20	1.1.5
	+ changed default menu mode, now main menu temporary appears when Alt is pressed

2010-06-19	1.1
	+ shows popup menu on Alt key if main menu is hidden
	+ unload protection on cm_UnloadPlugins (loads itself to increase loads count)

2010-06-19	1.0
	! first public release
	+ show/hide menu feature
	+ shows main menu as popup menu
	+ shows empty line for HELP_BREAK
	+ controlled by windows messages sent to TC window
