# Class-Automate
import schedule
import time
import webbrowser
import datetime
import easygui
from easygui import *


def weblink(subj):
    if subj == "ds" or subj == "DS":
        return "https://meet.google.com/lookup/dphptsrpl2"
    elif subj == "df" or subj == "DF":
        return "https://meet.google.com/lookup/hmzooc5bqe"
    elif subj == "ps" or subj == "P&S":
        return "https://meet.google.com/lookup/fiivjb53y2"
    elif subj == "ic" or subj == "IC":
        return "https://meet.google.com/lookup/feapg4vzrr"
    elif subj == "dbms" or subj == "DBMS":
        return "https://meet.google.com/lookup/e6rcrkgsis"
    elif subj == "de1a" or subj == "DE-1A":
        return "https://meet.google.com/lookup/awtx6ghufc"
    elif subj == "etc" or subj == "ETC":
        return "https://meet.google.com/lookup/btz5h2rcll"


def new():
    text = "Please select the lecture from below"
    title = "Classroom"
    choices = ["DS", "DF", "IC", "DBMS", "ETC", "DE-1A", "P&S"]
    op = choicebox(text, title, choices)
    if op == "DS":
        webbrowser.open_new(weblink("ds"))
    elif op == "DF":
        webbrowser.open_new(weblink("df"))
    elif op == "IC":
        webbrowser.open_new(weblink("ic"))
    elif op == "DBMS":
        webbrowser.open_new(weblink("dbms"))
    elif op == "ETC":
        webbrowser.open_new(weblink("etc"))
    elif op == "DE-1A":
        webbrowser.open_new(weblink("de1a"))
    elif op == "P&S":
        webbrowser.open_new(weblink("ps"))


def jobm():
    now = datetime.datetime.now()
    hm = now.strftime('%H:%M')
    if hm == "08:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            ans = ynbox("What is you Batch ?\nIf it's Batch A than click YES\n If it's Batch B click No", "Classroom")
            if ans == 'yes':
                easygui.msgbox("Remainder for DF class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("df"))
            else:
                easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("ds"))
    elif hm == "10:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for P&S class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ps"))
    elif hm == "11:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DBMS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("dbms"))
    elif hm == "13:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ds"))
    elif hm == "14:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Time is 2:28\nTime for DBMS class", title="Classroom")
            webbrowser.open_new(weblink("dbms"))


def jobt():
    now = datetime.datetime.now()
    hm = now.strftime('%H:%M')
    if hm == "08:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for IC class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ic"))
    elif hm == "09:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            ans = ynbox("What is you Batch ?\nIf it's Batch A than click YES or click NO", "Classroom")
            if ans == 'yes':
                easygui.msgbox("Remainder for DBMS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("dbms"))
            else:
                easygui.msgbox("Remainder for ETC class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("etc"))
    elif hm == "11:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DF class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("df"))
    elif hm == "13:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for ETC class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("etc"))
    elif hm == "14:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for P&S(T) class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ps"))


def jobw():
    now = datetime.datetime.now()
    hm = now.strftime('%H:%M')
    if hm == "08:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            ans = ynbox("What is you Batch ?\nIf it's Batch Batch A than click YES or click NO", "Classroom")
            if ans == 'yes':
                easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("ds"))
            else:
                easygui.msgbox("Remainder for DF class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("df"))
    elif hm == "10:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DBMS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("dbms"))
    elif hm == "11:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ds"))
    elif hm == "13:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DF class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("df"))
    elif hm == "14:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        print(a)
        if a:
            new()
        else:
            easygui.msgbox("Remainder for P&S class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ps"))


def jobth():
    now = datetime.datetime.now()
    hm = now.strftime('%H:%M')
    if hm == "08:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for IC class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ic"))
    elif hm == "09:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ds"))
    elif hm == "10:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for ETC class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("etc"))
    elif hm == "11:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for P&S class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ps"))
    elif hm == "13:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            ans = ynbox("What is you Batch ?\nIf it's Batch A than click YES or click NO", "Classroom")
            if ans == 'yes':
                easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("ds"))
            else:
                easygui.msgbox("Remainder for DBMS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("dbms"))


def jobf():
    now = datetime.datetime.now()
    hm = now.strftime('%H:%M')
    if hm == "08:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DF class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("df"))
    elif hm == "09:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for P&S class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("ps"))
    elif hm == "10:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DBMS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("dbms"))
    elif hm == "11:45":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            ans = ynbox("What is you Batch ?\nIf it's Batch A than click YES or click NO", "Classroom")
            if ans == 'yes':
                easygui.msgbox("Remainder for ETC class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("etc"))
            else:
                easygui.msgbox("Remainder for DS class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
                webbrowser.open_new(weblink("ds"))
    elif hm == "14:30":
        a = ynbox("Is lecture for this time is changed to some other time ?\n[If mam has scheduled class of this time at some other time select YES else select NO] ?. ", title="Classroom")
        if a:
            new()
        else:
            easygui.msgbox("Remainder for DE-1A class.\nBy clicking OK you would be directed to class instantly .", title="Classroom")
            webbrowser.open_new(weblink("de1a"))


def main():
    print("---------------------------------------------------")
    print("                 Hello Student")
    print("---------------------------------------------------")
    now = datetime.datetime.now()
    hm = now.strftime('%H:%M')
    d = now.strftime('%A')
    if "08:00" <= hm <= "15:00":
        now = datetime.datetime.now()
        hm = now.strftime('%H:%M')
        d = now.strftime('%A')
        print("Today is", d)
        print("Python Script has been started in background.\nJust do not close this window...")
        print("All classes would now get automatically started..")
        if d == "Monday":
            schedule.every().monday.at("08:30").do(jobm)
            schedule.every().monday.at("10:45").do(jobm)
            schedule.every().monday.at("11:45").do(jobm)
            schedule.every().monday.at("13:30").do(jobm)
            schedule.every().monday.at("14:30").do(jobm)
        if d == "Tuesday":
            schedule.every().tuesday.at("08:30").do(jobt)
            schedule.every().tuesday.at("09:30").do(jobt)
            schedule.every().tuesday.at("11:45").do(jobt)
            schedule.every().tuesday.at("13:30").do(jobt)
            schedule.every().tuesday.at("14:30").do(jobt)
        if d == "Wednesday":
            schedule.every().wednesday.at("08:30").do(jobw)
            schedule.every().wednesday.at("10:45").do(jobw)
            schedule.every().wednesday.at("11:45").do(jobw)
            schedule.every().wednesday.at("13:30").do(jobw)
            schedule.every().wednesday.at("14:30").do(jobw)
        if d == "Thursday":
            schedule.every().thursday.at("08:30").do(jobth)
            schedule.every().thursday.at("09:30").do(jobth)
            schedule.every().thursday.at("10:45").do(jobth)
            schedule.every().thursday.at("11:45").do(jobth)
            schedule.every().thursday.at("13:30").do(jobth)
        if d == "Friday":
            schedule.every().friday.at("08:30").do(jobf)
            schedule.every().friday.at("09:30").do(jobf)
            schedule.every().friday.at("10:45").do(jobf)
            schedule.every().friday.at("11:45").do(jobf)
            schedule.every().friday.at("14:30").do(jobf)
        while True:
            schedule.run_pending()
            time.sleep(1)
    elif d == "Saturday":
        a = ynbox("Today is Saturday.\nAre there any lectures today?", title="Classroom")
        new()
    else:
        print("Currently no classes are going on.")
        print("Classes would now resume from 8:30 A.M.")
        print("---------------------------------------------------")
    a = input("Press any key to exit.")

main()
