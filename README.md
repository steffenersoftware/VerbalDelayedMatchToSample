#!/usr/bin/env python2
# -*- coding: utf-8 -*-
"""
This experiment was created using PsychoPy2 Experiment Builder (v1.84.2),
    on Thu  1 Jun 12:09:10 2017
If you publish work using this script please cite the PsychoPy publications:
    Peirce, JW (2007) PsychoPy - Psychophysics software in Python.
        Journal of Neuroscience Methods, 162(1-2), 8-13.
    Peirce, JW (2009) Generating stimuli for neuroscience using PsychoPy.
        Frontiers in Neuroinformatics, 2:10. doi: 10.3389/neuro.11.010.2008
"""

from __future__ import absolute_import, division
from psychopy import locale_setup, gui, visual, core, data, event, logging, sound
from psychopy.constants import (NOT_STARTED, STARTED, PLAYING, PAUSED,
                                STOPPED, FINISHED, PRESSED, RELEASED, FOREVER)
import numpy as np  # whole numpy lib is available, prepend 'np.'
from numpy import (sin, cos, tan, log, log10, pi, average,
                   sqrt, std, deg2rad, rad2deg, linspace, asarray)
from numpy.random import random, randint, normal, shuffle
import os  # handy system and path functions
import sys  # to get file system encoding

# Ensure that relative paths start from the same directory as this script
_thisDir = os.path.dirname(os.path.abspath(__file__)).decode(sys.getfilesystemencoding())
os.chdir(_thisDir)

# Store info about the experiment session
expName = 'attemptDMS'  # from the Builder filename that created this script
expInfo = {'participant':'', 'session':'001'}
dlg = gui.DlgFromDict(dictionary=expInfo, title=expName)
if dlg.OK == False:
    core.quit()  # user pressed cancel
expInfo['date'] = data.getDateStr()  # add a simple timestamp
expInfo['expName'] = expName

# Data file name stem = absolute path + name; later add .psyexp, .csv, .log, etc
filename = _thisDir + os.sep + u'data/%s_%s_%s' % (expInfo['participant'], expName, expInfo['date'])

# An ExperimentHandler isn't essential but helps with data saving
thisExp = data.ExperimentHandler(name=expName, version='',
    extraInfo=expInfo, runtimeInfo=None,
    originPath=None,
    savePickle=True, saveWideText=True,
    dataFileName=filename)
# save a log file for detail verbose info
logFile = logging.LogFile(filename+'.log', level=logging.EXP)
logging.console.setLevel(logging.WARNING)  # this outputs to the screen, not a file

endExpNow = False  # flag for 'escape' or other condition => quit the exp

# Start Code - component code to be run before the window creation

# Setup the Window
win = visual.Window(
    size=(1280, 800), fullscr=True, screen=0,
    allowGUI=False, allowStencil=False,
    monitor='testMonitor', color=[0,0,0], colorSpace='rgb',
    blendMode='avg', useFBO=True)
# store frame rate of monitor if we can measure it
expInfo['frameRate'] = win.getActualFrameRate()
if expInfo['frameRate'] != None:
    frameDur = 1.0 / round(expInfo['frameRate'])
else:
    frameDur = 1.0 / 60.0  # could not measure, so guess

# Initialize components for Routine "Instructions"
InstructionsClock = core.Clock()
textInstructions = visual.TextStim(win=win, name='textInstructions',
    text='Ready to start the main experiment?\n\nRemember:\nPress [LEFT] if the letter WAS in the set.\nPress [DOWN] if the letter was NOT in the set.\n\nTry to respond as quickly and as accurately as possible.\n\nWhen you are ready to proceed press any key.',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='yellow', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "IntroDelay"
IntroDelayClock = core.Clock()
textIntroDelay = visual.TextStim(win=win, name='textIntroDelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Interblock"
InterblockClock = core.Clock()
textInterblock = visual.TextStim(win=win, name='textInterblock',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='red', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "ITI"
ITIClock = core.Clock()
textITI = visual.TextStim(win=win, name='textITI',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "trial"
trialClock = core.Clock()
textTL = visual.TextStim(win=win, name='textTL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);
textTM = visual.TextStim(win=win, name='textTM',
    text='default text',
    font='Courier',
    pos=(0, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-1.0);
textTR = visual.TextStim(win=win, name='textTR',
    text='default text',
    font='Courier',
    pos=(0.15, 0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-2.0);
textCL = visual.TextStim(win=win, name='textCL',
    text='default text',
    font='Courier',
    pos=(-0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-3.0);
textCM = visual.TextStim(win=win, name='textCM',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-4.0);
textCR = visual.TextStim(win=win, name='textCR',
    text='default text',
    font='Courier',
    pos=(0.15, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-5.0);
textBL = visual.TextStim(win=win, name='textBL',
    text='default text',
    font='Courier',
    pos=(-0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-6.0);
textBM = visual.TextStim(win=win, name='textBM',
    text='default text',
    font='Courier',
    pos=(0, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-7.0);
textBR = visual.TextStim(win=win, name='textBR',
    text='default text',
    font='Courier',
    pos=(0.15, -0.15), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=-8.0);

# Initialize components for Routine "delay"
delayClock = core.Clock()
textdelay = visual.TextStim(win=win, name='textdelay',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "probe"
probeClock = core.Clock()
textprobe = visual.TextStim(win=win, name='textprobe',
    text='default text',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='green', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "EndDelay"
EndDelayClock = core.Clock()
text = visual.TextStim(win=win, name='text',
    text='+',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='white', colorSpace='rgb', opacity=1,
    depth=0.0);

# Initialize components for Routine "Thankyou"
ThankyouClock = core.Clock()
textThankyou = visual.TextStim(win=win, name='textThankyou',
    text='Thank you for participating!\n\nWhen you are ready to proceed press any key.',
    font='Courier',
    pos=(0, 0), height=0.1, wrapWidth=None, ori=0, 
    color='yellow', colorSpace='rgb', opacity=1,
    depth=0.0);

# Create some handy timers
globalClock = core.Clock()  # to track the time since experiment started
routineTimer = core.CountdownTimer()  # to track time remaining of each (non-slip) routine 

# ------Prepare to start Routine "Instructions"-------
t = 0
InstructionsClock.reset()  # clock
frameN = -1
continueRoutine = True
# update component parameters for each repeat
key_resp_3 = event.BuilderKeyResponse()
# keep track of which components have finished
InstructionsComponents = [textInstructions, key_resp_3]
for thisComponent in InstructionsComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Instructions"-------
while continueRoutine:
    # get current time
    t = InstructionsClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInstructions* updates
    if t >= 0.0 and textInstructions.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInstructions.tStart = t
        textInstructions.frameNStart = frameN  # exact frame index
        textInstructions.setAutoDraw(True)
    
    # *key_resp_3* updates
    if t >= 0.0 and key_resp_3.status == NOT_STARTED:
        # keep track of start time/frame for later
        key_resp_3.tStart = t
        key_resp_3.frameNStart = frameN  # exact frame index
        key_resp_3.status = STARTED
        # keyboard checking is just starting
        event.clearEvents(eventType='keyboard')
    if key_resp_3.status == STARTED:
        theseKeys = event.getKeys()
        
        # check for quit:
        if "escape" in theseKeys:
            endExpNow = True
        if len(theseKeys) > 0:  # at least one key was pressed
            # a response ends the routine
            continueRoutine = False
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InstructionsComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Instructions"-------
for thisComponent in InstructionsComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)
# the Routine "Instructions" was not non-slip safe, so reset the non-slip timer
routineTimer.reset()

# ------Prepare to start Routine "IntroDelay"-------
t = 0
IntroDelayClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(2.000000)
# update component parameters for each repeat
# keep track of which components have finished
IntroDelayComponents = [textIntroDelay]
for thisComponent in IntroDelayComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "IntroDelay"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = IntroDelayClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textIntroDelay* updates
    if t >= 0.0 and textIntroDelay.status == NOT_STARTED:
        # keep track of start time/frame for later
        textIntroDelay.tStart = t
        textIntroDelay.frameNStart = frameN  # exact frame index
        textIntroDelay.setAutoDraw(True)
    frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textIntroDelay.status == STARTED and t >= frameRemains:
        textIntroDelay.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in IntroDelayComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "IntroDelay"-------
for thisComponent in IntroDelayComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials1 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile1.xlsx'),
    seed=None, name='trials1')
thisExp.addLoop(trials1)  # add the loop to the experiment
thisTrials1 = trials1.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials1.rgb)
if thisTrials1 != None:
    for paramName in thisTrials1.keys():
        exec(paramName + '= thisTrials1.' + paramName)

for thisTrials1 in trials1:
    currentLoop = trials1
    # abbreviate parameter names if possible (e.g. rgb = thisTrials1.rgb)
    if thisTrials1 != None:
        for paramName in thisTrials1.keys():
            exec(paramName + '= thisTrials1.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials1 (TrialHandler)
    trials1.addData('response1.keys',response1.keys)
    trials1.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials1.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials1'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials2 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile2.xlsx'),
    seed=None, name='trials2')
thisExp.addLoop(trials2)  # add the loop to the experiment
thisTrials2 = trials2.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials2.rgb)
if thisTrials2 != None:
    for paramName in thisTrials2.keys():
        exec(paramName + '= thisTrials2.' + paramName)

for thisTrials2 in trials2:
    currentLoop = trials2
    # abbreviate parameter names if possible (e.g. rgb = thisTrials2.rgb)
    if thisTrials2 != None:
        for paramName in thisTrials2.keys():
            exec(paramName + '= thisTrials2.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials2 (TrialHandler)
    trials2.addData('response1.keys',response1.keys)
    trials2.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials2.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials2'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials3 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile3.xlsx'),
    seed=None, name='trials3')
thisExp.addLoop(trials3)  # add the loop to the experiment
thisTrials3 = trials3.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials3.rgb)
if thisTrials3 != None:
    for paramName in thisTrials3.keys():
        exec(paramName + '= thisTrials3.' + paramName)

for thisTrials3 in trials3:
    currentLoop = trials3
    # abbreviate parameter names if possible (e.g. rgb = thisTrials3.rgb)
    if thisTrials3 != None:
        for paramName in thisTrials3.keys():
            exec(paramName + '= thisTrials3.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials3 (TrialHandler)
    trials3.addData('response1.keys',response1.keys)
    trials3.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials3.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials3'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials4 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile4.xlsx'),
    seed=None, name='trials4')
thisExp.addLoop(trials4)  # add the loop to the experiment
thisTrials4 = trials4.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials4.rgb)
if thisTrials4 != None:
    for paramName in thisTrials4.keys():
        exec(paramName + '= thisTrials4.' + paramName)

for thisTrials4 in trials4:
    currentLoop = trials4
    # abbreviate parameter names if possible (e.g. rgb = thisTrials4.rgb)
    if thisTrials4 != None:
        for paramName in thisTrials4.keys():
            exec(paramName + '= thisTrials4.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials4 (TrialHandler)
    trials4.addData('response1.keys',response1.keys)
    trials4.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials4.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials4'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials5 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile5.xlsx'),
    seed=None, name='trials5')
thisExp.addLoop(trials5)  # add the loop to the experiment
thisTrials5 = trials5.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials5.rgb)
if thisTrials5 != None:
    for paramName in thisTrials5.keys():
        exec(paramName + '= thisTrials5.' + paramName)

for thisTrials5 in trials5:
    currentLoop = trials5
    # abbreviate parameter names if possible (e.g. rgb = thisTrials5.rgb)
    if thisTrials5 != None:
        for paramName in thisTrials5.keys():
            exec(paramName + '= thisTrials5.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials5 (TrialHandler)
    trials5.addData('response1.keys',response1.keys)
    trials5.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials5.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials5'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials6 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile6.xlsx'),
    seed=None, name='trials6')
thisExp.addLoop(trials6)  # add the loop to the experiment
thisTrials6 = trials6.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials6.rgb)
if thisTrials6 != None:
    for paramName in thisTrials6.keys():
        exec(paramName + '= thisTrials6.' + paramName)

for thisTrials6 in trials6:
    currentLoop = trials6
    # abbreviate parameter names if possible (e.g. rgb = thisTrials6.rgb)
    if thisTrials6 != None:
        for paramName in thisTrials6.keys():
            exec(paramName + '= thisTrials6.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials6 (TrialHandler)
    trials6.addData('response1.keys',response1.keys)
    trials6.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials6.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials6'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials7 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile7.xlsx'),
    seed=None, name='trials7')
thisExp.addLoop(trials7)  # add the loop to the experiment
thisTrials7 = trials7.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials7.rgb)
if thisTrials7 != None:
    for paramName in thisTrials7.keys():
        exec(paramName + '= thisTrials7.' + paramName)

for thisTrials7 in trials7:
    currentLoop = trials7
    # abbreviate parameter names if possible (e.g. rgb = thisTrials7.rgb)
    if thisTrials7 != None:
        for paramName in thisTrials7.keys():
            exec(paramName + '= thisTrials7.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials7 (TrialHandler)
    trials7.addData('response1.keys',response1.keys)
    trials7.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials7.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials7'


# ------Prepare to start Routine "Interblock"-------
t = 0
InterblockClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(24.000000)
# update component parameters for each repeat
# keep track of which components have finished
InterblockComponents = [textInterblock]
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Interblock"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = InterblockClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textInterblock* updates
    if t >= 0.0 and textInterblock.status == NOT_STARTED:
        # keep track of start time/frame for later
        textInterblock.tStart = t
        textInterblock.frameNStart = frameN  # exact frame index
        textInterblock.setAutoDraw(True)
    frameRemains = 0.0 + 24.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if textInterblock.status == STARTED and t >= frameRemains:
        textInterblock.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in InterblockComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Interblock"-------
for thisComponent in InterblockComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# set up handler to look after randomisation of conditions etc
trials8 = data.TrialHandler(nReps=1, method='random', 
    extraInfo=expInfo, originPath=-1,
    trialList=data.importConditions('DMSFile8.xlsx'),
    seed=None, name='trials8')
thisExp.addLoop(trials8)  # add the loop to the experiment
thisTrials8 = trials8.trialList[0]  # so we can initialise stimuli with some values
# abbreviate parameter names if possible (e.g. rgb = thisTrials8.rgb)
if thisTrials8 != None:
    for paramName in thisTrials8.keys():
        exec(paramName + '= thisTrials8.' + paramName)

for thisTrials8 in trials8:
    currentLoop = trials8
    # abbreviate parameter names if possible (e.g. rgb = thisTrials8.rgb)
    if thisTrials8 != None:
        for paramName in thisTrials8.keys():
            exec(paramName + '= thisTrials8.' + paramName)
    
    # ------Prepare to start Routine "ITI"-------
    t = 0
    ITIClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(0.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    ITIComponents = [textITI]
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "ITI"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = ITIClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textITI* updates
        if t >= 0.0 and textITI.status == NOT_STARTED:
            # keep track of start time/frame for later
            textITI.tStart = t
            textITI.frameNStart = frameN  # exact frame index
            textITI.setAutoDraw(True)
        frameRemains = 0.0 + 0.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textITI.status == STARTED and t >= frameRemains:
            textITI.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in ITIComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "ITI"-------
    for thisComponent in ITIComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "trial"-------
    t = 0
    trialClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textTL.setText(TL)
    textTM.setText(TM)
    textTR.setText(TR)
    textCL.setText(CL)
    textCM.setText(CM)
    textCR.setText(CR)
    textBL.setText(BL)
    textBM.setText(BM)
    textBR.setText(BR)
    # keep track of which components have finished
    trialComponents = [textTL, textTM, textTR, textCL, textCM, textCR, textBL, textBM, textBR]
    for thisComponent in trialComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "trial"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = trialClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textTL* updates
        if t >= 0.0 and textTL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTL.tStart = t
            textTL.frameNStart = frameN  # exact frame index
            textTL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTL.status == STARTED and t >= frameRemains:
            textTL.setAutoDraw(False)
        
        # *textTM* updates
        if t >= 0.0 and textTM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTM.tStart = t
            textTM.frameNStart = frameN  # exact frame index
            textTM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTM.status == STARTED and t >= frameRemains:
            textTM.setAutoDraw(False)
        
        # *textTR* updates
        if t >= 0.0 and textTR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textTR.tStart = t
            textTR.frameNStart = frameN  # exact frame index
            textTR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textTR.status == STARTED and t >= frameRemains:
            textTR.setAutoDraw(False)
        
        # *textCL* updates
        if t >= 0.0 and textCL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCL.tStart = t
            textCL.frameNStart = frameN  # exact frame index
            textCL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCL.status == STARTED and t >= frameRemains:
            textCL.setAutoDraw(False)
        
        # *textCM* updates
        if t >= 0.0 and textCM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCM.tStart = t
            textCM.frameNStart = frameN  # exact frame index
            textCM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCM.status == STARTED and t >= frameRemains:
            textCM.setAutoDraw(False)
        
        # *textCR* updates
        if t >= 0.0 and textCR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textCR.tStart = t
            textCR.frameNStart = frameN  # exact frame index
            textCR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textCR.status == STARTED and t >= frameRemains:
            textCR.setAutoDraw(False)
        
        # *textBL* updates
        if t >= 0.0 and textBL.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBL.tStart = t
            textBL.frameNStart = frameN  # exact frame index
            textBL.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBL.status == STARTED and t >= frameRemains:
            textBL.setAutoDraw(False)
        
        # *textBM* updates
        if t >= 0.0 and textBM.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBM.tStart = t
            textBM.frameNStart = frameN  # exact frame index
            textBM.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBM.status == STARTED and t >= frameRemains:
            textBM.setAutoDraw(False)
        
        # *textBR* updates
        if t >= 0.0 and textBR.status == NOT_STARTED:
            # keep track of start time/frame for later
            textBR.tStart = t
            textBR.frameNStart = frameN  # exact frame index
            textBR.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textBR.status == STARTED and t >= frameRemains:
            textBR.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in trialComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "trial"-------
    for thisComponent in trialComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "delay"-------
    t = 0
    delayClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.500000)
    # update component parameters for each repeat
    # keep track of which components have finished
    delayComponents = [textdelay]
    for thisComponent in delayComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "delay"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = delayClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textdelay* updates
        if t >= 0.0 and textdelay.status == NOT_STARTED:
            # keep track of start time/frame for later
            textdelay.tStart = t
            textdelay.frameNStart = frameN  # exact frame index
            textdelay.setAutoDraw(True)
        frameRemains = 0.0 + 2.5- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textdelay.status == STARTED and t >= frameRemains:
            textdelay.setAutoDraw(False)
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in delayComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "delay"-------
    for thisComponent in delayComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    
    # ------Prepare to start Routine "probe"-------
    t = 0
    probeClock.reset()  # clock
    frameN = -1
    continueRoutine = True
    routineTimer.add(2.000000)
    # update component parameters for each repeat
    textprobe.setText(probe)
    response1 = event.BuilderKeyResponse()
    # keep track of which components have finished
    probeComponents = [textprobe, response1]
    for thisComponent in probeComponents:
        if hasattr(thisComponent, 'status'):
            thisComponent.status = NOT_STARTED
    
    # -------Start Routine "probe"-------
    while continueRoutine and routineTimer.getTime() > 0:
        # get current time
        t = probeClock.getTime()
        frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
        # update/draw components on each frame
        
        # *textprobe* updates
        if t >= 0.0 and textprobe.status == NOT_STARTED:
            # keep track of start time/frame for later
            textprobe.tStart = t
            textprobe.frameNStart = frameN  # exact frame index
            textprobe.setAutoDraw(True)
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if textprobe.status == STARTED and t >= frameRemains:
            textprobe.setAutoDraw(False)
        
        # *response1* updates
        if t >= 0.0 and response1.status == NOT_STARTED:
            # keep track of start time/frame for later
            response1.tStart = t
            response1.frameNStart = frameN  # exact frame index
            response1.status = STARTED
            # keyboard checking is just starting
            win.callOnFlip(response1.clock.reset)  # t=0 on next screen flip
        frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
        if response1.status == STARTED and t >= frameRemains:
            response1.status = STOPPED
        if response1.status == STARTED:
            theseKeys = event.getKeys(keyList=['left', 'down'])
            
            # check for quit:
            if "escape" in theseKeys:
                endExpNow = True
            if len(theseKeys) > 0:  # at least one key was pressed
                response1.keys = theseKeys[-1]  # just the last key pressed
                response1.rt = response1.clock.getTime()
                # was this 'correct'?
                if (response1.keys == str(corr)) or (response1.keys == corr):
                    response1.corr = 1
                else:
                    response1.corr = 0
        
        # check if all components have finished
        if not continueRoutine:  # a component has requested a forced-end of Routine
            break
        continueRoutine = False  # will revert to True if at least one component still running
        for thisComponent in probeComponents:
            if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
                continueRoutine = True
                break  # at least one component has not yet finished
        
        # check for quit (the Esc key)
        if endExpNow or event.getKeys(keyList=["escape"]):
            core.quit()
        
        # refresh the screen
        if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
            win.flip()
    
    # -------Ending Routine "probe"-------
    for thisComponent in probeComponents:
        if hasattr(thisComponent, "setAutoDraw"):
            thisComponent.setAutoDraw(False)
    # check responses
    if response1.keys in ['', [], None]:  # No response was made
        response1.keys=None
        # was no response the correct answer?!
        if str(corr).lower() == 'none':
           response1.corr = 1  # correct non-response
        else:
           response1.corr = 0  # failed to respond (incorrectly)
    # store data for trials8 (TrialHandler)
    trials8.addData('response1.keys',response1.keys)
    trials8.addData('response1.corr', response1.corr)
    if response1.keys != None:  # we had a response
        trials8.addData('response1.rt', response1.rt)
    thisExp.nextEntry()
    
# completed 1 repeats of 'trials8'


# ------Prepare to start Routine "EndDelay"-------
t = 0
EndDelayClock.reset()  # clock
frameN = -1
continueRoutine = True
routineTimer.add(2.000000)
# update component parameters for each repeat
# keep track of which components have finished
EndDelayComponents = [text]
for thisComponent in EndDelayComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "EndDelay"-------
while continueRoutine and routineTimer.getTime() > 0:
    # get current time
    t = EndDelayClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *text* updates
    if t >= 0.0 and text.status == NOT_STARTED:
        # keep track of start time/frame for later
        text.tStart = t
        text.frameNStart = frameN  # exact frame index
        text.setAutoDraw(True)
    frameRemains = 0.0 + 2.0- win.monitorFramePeriod * 0.75  # most of one frame period left
    if text.status == STARTED and t >= frameRemains:
        text.setAutoDraw(False)
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in EndDelayComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "EndDelay"-------
for thisComponent in EndDelayComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)

# ------Prepare to start Routine "Thankyou"-------
t = 0
ThankyouClock.reset()  # clock
frameN = -1
continueRoutine = True
# update component parameters for each repeat
key_resp_2 = event.BuilderKeyResponse()
# keep track of which components have finished
ThankyouComponents = [textThankyou, key_resp_2]
for thisComponent in ThankyouComponents:
    if hasattr(thisComponent, 'status'):
        thisComponent.status = NOT_STARTED

# -------Start Routine "Thankyou"-------
while continueRoutine:
    # get current time
    t = ThankyouClock.getTime()
    frameN = frameN + 1  # number of completed frames (so 0 is the first frame)
    # update/draw components on each frame
    
    # *textThankyou* updates
    if t >= 0.0 and textThankyou.status == NOT_STARTED:
        # keep track of start time/frame for later
        textThankyou.tStart = t
        textThankyou.frameNStart = frameN  # exact frame index
        textThankyou.setAutoDraw(True)
    
    # *key_resp_2* updates
    if t >= 0.0 and key_resp_2.status == NOT_STARTED:
        # keep track of start time/frame for later
        key_resp_2.tStart = t
        key_resp_2.frameNStart = frameN  # exact frame index
        key_resp_2.status = STARTED
        # keyboard checking is just starting
        event.clearEvents(eventType='keyboard')
    if key_resp_2.status == STARTED:
        theseKeys = event.getKeys()
        
        # check for quit:
        if "escape" in theseKeys:
            endExpNow = True
        if len(theseKeys) > 0:  # at least one key was pressed
            # a response ends the routine
            continueRoutine = False
    
    # check if all components have finished
    if not continueRoutine:  # a component has requested a forced-end of Routine
        break
    continueRoutine = False  # will revert to True if at least one component still running
    for thisComponent in ThankyouComponents:
        if hasattr(thisComponent, "status") and thisComponent.status != FINISHED:
            continueRoutine = True
            break  # at least one component has not yet finished
    
    # check for quit (the Esc key)
    if endExpNow or event.getKeys(keyList=["escape"]):
        core.quit()
    
    # refresh the screen
    if continueRoutine:  # don't flip if this routine is over or we'll get a blank screen
        win.flip()

# -------Ending Routine "Thankyou"-------
for thisComponent in ThankyouComponents:
    if hasattr(thisComponent, "setAutoDraw"):
        thisComponent.setAutoDraw(False)
# the Routine "Thankyou" was not non-slip safe, so reset the non-slip timer
routineTimer.reset()
# these shouldn't be strictly necessary (should auto-save)
thisExp.saveAsWideText(filename+'.csv')
thisExp.saveAsPickle(filename)
logging.flush()
# make sure everything is closed down
thisExp.abort()  # or data files will save again on exit
win.close()
core.quit()
