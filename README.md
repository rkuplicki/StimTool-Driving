# StimTool-Driving
Repo for sharing the driving component of StimTool


Installation Instructions:
All necessary files are under InstallationFiles/

Install PsychoPy (via StandalonePsychoPy-1.80.03-win32.exe, used for all components)
Update PsychoPy to 1.80.06 using PsychoPy-1.80.06.zip (i.e. open PsychoPy and go Tools->PsychoPy Updates->Use zip file and select it
This contains various bug fixes.
Yes--1.80.06 is an ancient version of PsychoPy (circa 2014), and it would be nice to update to PsychoPy 3.
Updating all of the code for this and ~30 other modules (tasks or tools) is on the list, just as soon as someone has time to do it and verify that everything still works.

Modify two lines in C:\Program Files (x86)\PsychoPy2\Lib\site-packages\PsychoPy-1.80.03-py2.7.egg\psychopy\hardware\joystick\pyglet_input\directinput.py
        This is a bug in this version of PsychoPy and was likely fixed (and no longer necessary) in a future release
        These changes are needed to use the joystick
        On lines 131 and 150, change _dispatch_events = dispatch_events (remove the underscore)
Install ASIO4ALL
        Right now, this is necessary to decrease sound latency.  You may not need to take this step depending on your sound card/drivers.
        ASIO4ALL_2_11_English.exe
        Test latency by running sound_test.py.
                An 'X' will appear and disappear a few times--there should also be a burst of white noise that occurs simultaneously if things are working properly.  If things are not, there may be a delay of ~400ms.


After installing psychopy, put StimTool-Driving under C:\

To run the driving task, either run StimTool-shortcut or open PsychoPy coder view, then open the StimTool.py script and run it.
This will open a dialogue box where you can enter a subject ID, administrator ID, and then select an Experiment Order (.TL file).
Typically this has a list of tasks to run, but here Driving is the only one available and so that .TL will run the driving task.
Output will be stored under C:\StimTool-Driving-TemporaryStorage (configurable in JustDriving.params).

For details about the trial structure and and output codes, see Driving/README.Driving.



