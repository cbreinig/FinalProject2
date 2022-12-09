import csv
from plan import *
from PyQt5.QtWidgets import *

QtWidgets.QApplication.setAttribute(QtCore.Qt.AA_EnableHighDpiScaling, True)
QtWidgets.QApplication.setAttribute(QtCore.Qt.AA_UseHighDpiPixmaps, True)


class Controller(QMainWindow, Ui_MainWindow):
    """
    A class representing details for a controller object
    :param QMainWindow: Main window tool that will act as a get for the user interface.
    :param Ui_MainWindow: Main window that will initialize the user interface.
    """

    def __init__(self, *args, **kwargs):
        """
        Constructor to create initial state of Controller object.
        :param args:variable pass for non-keyword arguments.
        :param kwargs: variable pass for keyword arguments.
        """
        super().__init__(*args, **kwargs)
        """
        Constructor avoid the base class explicitly.
        :param args:variable pass for non-keyword arguments.
        :param kwargs: variable pass for keyword arguments.
        """
        self.setupUi(self)
        self.pushButton.clicked.connect(lambda: self.submit())
        self.pushButton_2.clicked.connect(lambda: self.clear())
        self.lineEdit.setText("")
        self.lineEdit_2.setText("")
        self.lineEdit_3.setText("45")
        self.lineEdit_4.setText("45")
        self.lineEdit_5.setText("45")
        """
        Method to setup the base UI.
        """

    def submit(self):
        """
        Method to create a button that will initialize a CSV generation based on a selection of radio buttons.
        :return: CSV file based off input.
        """
        try:
            """
            Method used to get int values from text input in the UI
            """
            height = int(self.lineEdit.text())
            weight = int(self.lineEdit_2.text())
            bench = int(self.lineEdit_3.text())
            squat = int(self.lineEdit_4.text())
            clean = int(self.lineEdit_5.text())
            bmi = weight / (height * height)

            if self.radioButton.isChecked():
                """
                Method used to check if RadioButton is selected when the submit button is clicked
                """
                with open('workout_plan.csv', 'w') as file:
                    """
                    Method used to generate a csv file based on int values from text input in the UI in the get
                    """
                    writer = csv.writer(file)
                    writer.writerow(["Week 1"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .4), " x 5 ", int(clean * .5), " x 5 ",
                         int(clean * .6), " x 5 ", int(clean * .65), " x 5 ", int(clean * .65), " x 5 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .4), " x 8 ", int(bench * .5), " x 8 ", int(bench * .55),
                         " x 8 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .25), " x 8", int(bench * .3), " x 8",
                         int(bench * .325),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .45), " x 8 ", int(bench * .5), " x 6-8 ", int(bench * .55),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 4 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .4), " x 15 ", int(squat * .5), " x 12 ", int(squat * .6), " x 10 ",
                         int(squat * .65), " x 10 ", int(squat * .65), " x 10 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .25), " x 5 ", int(squat * .3), " x 5 ",
                                     int(squat * .325), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["3 x 300 yards"])
                    if bmi > 30:
                        writer.writerow(["60 seconds to complete"])
                    else:
                        writer.writerow(["50 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .4), " x 15 ", int(bench * .5), " x 12 ", int(bench * .6),
                         " x 10 ", int(bench * .65), " x 10 ", int(bench * .65), " x 10 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .25), " x 5 ", int(bench * .3), " x 5 ", int(bench * .325),
                         " x 5 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .2), " x 5 ", int(bench * .24), " x 5 ",
                         int(bench * .27),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .25), " x 5 ", int(clean * .3), " x 5 ", int(clean * .325),
                         " x 5 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 5 "])
                    writer.writerow([
                                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["10 x 110 sprints, 30 second rest between reps"])
                    if bmi > 30:
                        writer.writerow(["21 seconds to complete"])
                    else:
                        writer.writerow(["17 seconds to complete"])

                    writer.writerow(["Week 2"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .5), " x 5 ", int(clean * .6), " x 5 ",
                         int(clean * .7), " x 3 ", int(clean * .7), " x 3 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 8 ", int(bench * .7),
                         " x 8 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .25), " x 8", int(bench * .3), " x 8",
                         int(bench * .325),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .45), " x 8 ", int(bench * .5), " x 6-8 ", int(bench * .55),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 4 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .5), " x 8 ", int(squat * .6), " x 6 ", int(squat * .7), " x 4 ",
                         int(squat * .7), " x 4 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .25), " x 5 ", int(squat * .3), " x 5 ",
                                     int(squat * .325), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 full gassers, 2 half gassers, 2 50 yars sprints"])
                    if bmi > 30:
                        writer.writerow(["40, 19, 9 seconds to complete"])
                    else:
                        writer.writerow(["35,16,6 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 5 ", int(bench * .7), " x 5 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .25), " x 5 ", int(bench * .3), " x 5 ", int(bench * .325),
                         " x 5 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .2), " x 5 ", int(bench * .24), " x 5 ",
                         int(bench * .27),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .25), " x 3 ", int(clean * .3), " x 3 ", int(clean * .325),
                         " x 3 ", int(clean * .325),
                         " x 3 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 5 "])
                    writer.writerow([
                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["300 yard shuttle"])
                    if bmi > 30:
                        writer.writerow(["67 seconds to complete"])
                    else:
                        writer.writerow(["61 seconds to complete"])

                    writer.writerow(["Week 3"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .5), " x 5 ", int(clean * .6), " x 5 ",
                         int(clean * .7), " x 3 ", int(clean * .75), " x 3 ", int(clean * .75), " x 3 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .4), " x 8 ", int(bench * .5), " x 8 ", int(bench * .55),
                         " x 5 ", int(bench * .6), " x 5 ", int(bench * .65), " x 5 ", int(bench * .65),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .3), " x 8", int(bench * .35), " x 8",
                         int(bench * .4),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .45), " x 8 ", int(bench * .5), " x 6-8 ", int(bench * .55),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 6 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .5), " x 8 ", int(squat * .6), " x 6 ", int(squat * .7), " x 4 ",
                         int(squat * .75), " x 4 ", int(squat * .75), " x 4 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .27), " x 5 ", int(squat * .325), " x 5 ",
                                     int(squat * .35), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 full gassers, 2 half gassers, 2 50 yars sprints"])
                    if bmi > 30:
                        writer.writerow(["40, 19, 9 seconds to complete"])
                    else:
                        writer.writerow(["35,16,6 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 5-7 ", int(bench * .75), " x 3-5 ", int(bench * .75), " x 3-5 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .25), " x 8 ", int(bench * .3), " x 8 ", int(bench * .325),
                         " x 8 ", int(bench * .35),
                         " x 8 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .2), " x 5 ", int(bench * .24), " x 5 ",
                         int(bench * .27),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .25), " x 3 ", int(clean * .3), " x 3 ", int(clean * .325),
                         " x 3 ", int(clean * .35),
                         " x 3 ", int(clean * .35),
                         " x 3 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 3 ",
                         int(squat * .55), " x 3 ", int(squat * .55), " x 3 "])
                    writer.writerow([
                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["300 yard shuttle"])
                    if bmi > 30:
                        writer.writerow(["65 seconds to complete"])
                    else:
                        writer.writerow(["60 seconds to complete"])

                    writer.writerow(["Week 4"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .5), " x 8 ", int(clean * .6), " x 6 ",
                         int(clean * .7), " x 4 ", int(clean * .75), " x 4 ", int(clean * .75), " x 4 ",
                         int(clean * .8), " x 3 ", int(clean * .8), " x 3 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .4), " x 8 ", int(bench * .5), " x 8 ", int(bench * .55),
                         " x 5 ", int(bench * .6), " x 5 ", int(bench * .65), " x 5 ", int(bench * .65),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .3), " x 8", int(bench * .35), " x 8",
                         int(bench * .4),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .45), " x 8 ", int(bench * .5), " x 6-8 ", int(bench * .55),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 6 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .5), " x 8 ", int(squat * .6), " x 6 ", int(squat * .7), " x 4 ",
                         int(squat * .75), " x 4 ", int(squat * .75), " x 4 ", int(squat * .8), " x 3 ",
                         int(squat * .8), " x 3 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .3), " x 5 ", int(squat * .325), " x 5 ",
                                     int(squat * .35), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["6 x 110's 2 full gassers, 2 half gassers, 2 50 yars sprints, 1 minute rest"])
                    if bmi > 30:
                        writer.writerow(["21, 40, 19, 9 seconds to complete"])
                    else:
                        writer.writerow(["17, 35,16,6 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 5 ", int(bench * .75), " x 5 ", int(bench * .75), " x 5 ", int(bench * .8), " x 3 ",
                         int(bench * .8), " x 3 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .25), " x 8 ", int(bench * .3), " x 8 ", int(bench * .325),
                         " x 8 ", int(bench * .35),
                         " x 8 ", int(bench * .4),
                         " x 6-8 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .3), " x 8 ", int(bench * .34), " x 8 ",
                         int(bench * .38),
                         " x 8 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .25), " x 7 ", int(clean * .3), " x 5 ", int(clean * .325),
                         " x 3 ", int(clean * .35),
                         " x 3 ", int(clean * .4),
                         " x 3 ", int(clean * .4),
                         " x 3 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 3 ",
                         int(squat * .55), " x 3 ", int(squat * .55), " x 3 "])
                    writer.writerow([
                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["300 yard shuttle"])
                    if bmi > 30:
                        writer.writerow(["64 seconds to complete"])
                    else:
                        writer.writerow(["59 seconds to complete"])

                    writer.writerow(["Week 5"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .5), " x 8 ", int(clean * .6), " x 6 ",
                         int(clean * .7), " x 4 ", int(clean * .75), " x 4 ", int(clean * .75), " x 4 ",
                         int(clean * .8), " x 2 ", int(clean * .85), " x 2 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .4), " x 8 ", int(bench * .5), " x 8 ", int(bench * .55),
                         " x 5 ", int(bench * .6), " x 5 ", int(bench * .65), " x 5 ", int(bench * .65),
                         " x 5 ", int(bench * .7),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .35), " x 8", int(bench * .4), " x 8",
                         int(bench * .45),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .5), " x 8 ", int(bench * .55), " x 6-8 ", int(bench * .6),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 6 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .5), " x 8 ", int(squat * .6), " x 6 ", int(squat * .7), " x 4 ",
                         int(squat * .75), " x 4 ", int(squat * .75), " x 4 ", int(squat * .8), " x 2 ",
                         int(squat * .85), " x 2 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .4), " x 5 ", int(squat * .45), " x 5 ",
                                     int(squat * .5), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["6 x 110's 2 full gassers, 2 half gassers, 2 50 yars sprints, 1 minute rest"])
                    if bmi > 30:
                        writer.writerow(["20, 39, 18, 8 seconds to complete"])
                    else:
                        writer.writerow(["16, 34,15,5 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 5 ", int(bench * .75), " x 5 ", int(bench * .8), " x 3 ",
                         int(bench * .85), " x 3 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .25), " x 8 ", int(bench * .3), " x 8 ", int(bench * .325),
                         " x 8 ", int(bench * .4),
                         " x 6 ", int(bench * .45),
                         " x 6 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .32), " x 8 ", int(bench * .37), " x 8 ",
                         int(bench * .4),
                         " x 8 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .25), " x 3 ", int(clean * .3), " x 3 ", int(clean * .325),
                         " x 3 ", int(clean * .35),
                         " x 3 ", int(clean * .4),
                         " x 3 ", int(clean * .45),
                         " x 3 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 3 ",
                         int(squat * .55), " x 3 ", int(squat * .6), " x 2 ", int(squat * .65), " x 2 "])
                    writer.writerow([
                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2x300 yard shuttle, 5 min rest"])
                    if bmi > 30:
                        writer.writerow(["64 seconds to complete"])
                    else:
                        writer.writerow(["59 seconds to complete"])

                    writer.writerow(["Week 6"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .5), " x 8 ", int(clean * .6), " x 6 ",
                         int(clean * .7), " x 4 ", int(clean * .75), " x 4 ", int(clean * .75), " x 4 ",
                         int(clean * .8), " x 2 ", int(clean * .85), " x 2 ", int(clean * .9), " x 1 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .4), " x 8 ", int(bench * .5), " x 8 ", int(bench * .55),
                         " x 5 ", int(bench * .6), " x 5 ", int(bench * .65), " x 5 ", int(bench * .65),
                         " x 5 ", int(bench * .7),
                         " x 5 ", int(bench * .75),
                         " x 2-5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .35), " x 8", int(bench * .4), " x 8",
                         int(bench * .45),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .5), " x 8 ", int(bench * .55), " x 6-8 ", int(bench * .6),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 6 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .5), " x 8 ", int(squat * .6), " x 6 ", int(squat * .7), " x 4 ",
                         int(squat * .75), " x 4 ", int(squat * .75), " x 4 ", int(squat * .8), " x 3 ",
                         int(squat * .85), " x 3 ",
                         int(squat * .9), " x 2-4 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .45), " x 8 ", int(squat * .5), " x 8 ",
                                     int(squat * .55), " x 8 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["6 x 110's 2 full gassers, 2 half gassers, 2 50 yars sprints, 1 minute rest"])
                    if bmi > 30:
                        writer.writerow(["20, 39, 18, 8 seconds to complete"])
                    else:
                        writer.writerow(["16, 34,15,5 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 5 ", int(bench * .75), " x 5 ", int(bench * .8), " x 3 ",
                         int(bench * .85), " x 3 ", int(bench * .9), " x 2-4 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .25), " x 8 ", int(bench * .3), " x 8 ", int(bench * .325),
                         " x 8 ", int(bench * .4),
                         " x 6 ", int(bench * .45),
                         " x 6 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .32), " x 8 ", int(bench * .37), " x 8 ",
                         int(bench * .4),
                         " x 8 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .25), " x 3 ", int(clean * .3), " x 3 ", int(clean * .325),
                         " x 3 ", int(clean * .35),
                         " x 3 ", int(clean * .4),
                         " x 3 ", int(clean * .45),
                         " x 3 ", int(clean * .5),
                         " x 2-3 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 3 ",
                         int(squat * .55), " x 3 ", int(squat * .6), " x 2 ", int(squat * .65), " x 2 "])
                    writer.writerow([
                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2x300 yard shuttle, 5 min rest"])
                    if bmi > 30:
                        writer.writerow(["64 seconds to complete"])
                    else:
                        writer.writerow(["59 seconds to complete"])

                    """
                    Functions used to calculate and output rows to csv based on int values
                    """

            if self.radioButton_2.isChecked():
                """
                Method used to check if RadioButton_2 is selected when the submit button is clicked
                """
                if bmi > 30:
                    """
                    Method used to check if BMI int is greater than 30
                    """
                    with open('workout_plan.csv', 'w') as file:
                        """
                        Method used to generate a csv file based on int values from text input in the UI in the get
                        """
                        writer = csv.writer(file)
                        writer.writerow(["Week 1"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 4x100 s"])
                        writer.writerow(["Cycling: Tempo 80 min (50 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 50 min (20 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 4x50s"])
                        writer.writerow(["Cycling: Hill Reps 60 min (5x3 min/ 4 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Run: 30 min easy"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 90 min"])
                        writer.writerow(["Run: transition immediately after bike 10 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Swim: 30 min technique"])
                        writer.writerow(["Run: Aerobic Endurance 70 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 2"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x20, 5x40 s"])
                        writer.writerow(["Cycling: Tempo 80 min (50 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 50 min (30 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 200s/100s/50s"])
                        writer.writerow(["Cycling: Hill Reps 65 min (5x3 min/ 5 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Swim: 1,400m time trial"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 110 min"])
                        writer.writerow(["Run: transition immediately after bike 10 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Run: Aerobic Endurance 80 min"])
                        writer.writerow(["Cycling: Easy 20 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 3"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 4x100 s"])
                        writer.writerow(["Cycling: Tempo 80 min (50 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 50 min (20 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 4x50s"])
                        writer.writerow(["Cycling: Hill Reps 60 min (5x3 min/ 4 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Run: 30 min easy"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 90 min"])
                        writer.writerow(["Run: transition immediately after bike 10 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Swim: 30 min technique"])
                        writer.writerow(["Run: Aerobic Endurance 70 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 4"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x20, 5x40 s"])
                        writer.writerow(["Cycling: Tempo 80 min (50 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 50 min (30 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 200s/100s/50s"])
                        writer.writerow(["Cycling: Hill Reps 65 min (5x3 min/ 5 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Swim: 1,400m time trial"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 110 min"])
                        writer.writerow(["Run: transition immediately after bike 10 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Run: Aerobic Endurance 80 min"])
                        writer.writerow(["Cycling: Easy 20 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 5"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 4x100 s"])
                        writer.writerow(["Cycling: Tempo 80 min (50 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 50 min (20 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 4x50s"])
                        writer.writerow(["Cycling: Hill Reps 60 min (5x3 min/ 4 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Run: 30 min easy"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 90 min"])
                        writer.writerow(["Run: transition immediately after bike 10 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Swim: 30 min technique"])
                        writer.writerow(["Run: Aerobic Endurance 70 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 6"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x20, 5x40 s"])
                        writer.writerow(["Cycling: Tempo 80 min (50 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 50 min (30 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 200s/100s/50s"])
                        writer.writerow(["Cycling: Hill Reps 65 min (5x3 min/ 5 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Swim: 1,400m time trial"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 110 min"])
                        writer.writerow(["Run: transition immediately after bike 10 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Run: Aerobic Endurance 80 min"])
                        writer.writerow(["Cycling: Easy 20 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        """
                        Functions used to generate csv rows
                        """
                else:
                    """
                    Method used to check if BMI int is not a satisfiable condition in above If statement
                    """
                    with open('workout_plan.csv', 'w') as file:
                        """
                        Method used to generate a csv file based on int values from text input in the UI in the get
                        """
                        writer = csv.writer(file)
                        writer.writerow(["Week 1"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x100 s"])
                        writer.writerow(["Cycling: Tempo 90 min (60 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 60 min (30 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 5x50s"])
                        writer.writerow(["Cycling: Hill Reps 60-75 min (5x3 min/ 6 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Run: 30 min easy"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 90-120 min"])
                        writer.writerow(["Run: transition immediately after bike 15 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Swim: 30-45 min technique"])
                        writer.writerow(["Run: Aerobic Endurance 80 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 2"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x25, 5x50 s"])
                        writer.writerow(["Cycling: Tempo 90 min (60 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 60 min (40 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 400s/200s/100s"])
                        writer.writerow(["Cycling: Hill Reps 75 min (5x3 min/ 6 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Swim: 1,500m time trial"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 120 min"])
                        writer.writerow(["Run: transition immediately after bike 20 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Run: Aerobic Endurance 90 min"])
                        writer.writerow(["Cycling: Easy 30 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 3"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x100 s"])
                        writer.writerow(["Cycling: Tempo 90 min (60 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 60 min (30 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 5x50s"])
                        writer.writerow(["Cycling: Hill Reps 60-75 min (5x3 min/ 6 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Run: 30 min easy"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 90-120 min"])
                        writer.writerow(["Run: transition immediately after bike 15 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Swim: 30-45 min technique"])
                        writer.writerow(["Run: Aerobic Endurance 80 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 4"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x25, 5x50 s"])
                        writer.writerow(["Cycling: Tempo 90 min (60 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 60 min (40 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 400s/200s/100s"])
                        writer.writerow(["Cycling: Hill Reps 75 min (5x3 min/ 6 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Swim: 1,500m time trial"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 120 min"])
                        writer.writerow(["Run: transition immediately after bike 20 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Run: Aerobic Endurance 90 min"])
                        writer.writerow(["Cycling: Easy 30 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 5"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x100 s"])
                        writer.writerow(["Cycling: Tempo 90 min (60 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 60 min (30 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 5x50s"])
                        writer.writerow(["Cycling: Hill Reps 60-75 min (5x3 min/ 6 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Run: 30 min easy"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 90-120 min"])
                        writer.writerow(["Run: transition immediately after bike 15 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Swim: 30-45 min technique"])
                        writer.writerow(["Run: Aerobic Endurance 80 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Week 6"])
                        writer.writerow(["Monday"])
                        writer.writerow(["Swim: speed-endurance 5x25, 5x50 s"])
                        writer.writerow(["Cycling: Tempo 90 min (60 in zone)"])
                        writer.writerow(["Tuesday"])
                        writer.writerow(["Run: 60 min (40 min tempo)"])
                        writer.writerow(["Wednesday"])
                        writer.writerow(["Swim: Aerobic endurance (base) intervals 400s/200s/100s"])
                        writer.writerow(["Cycling: Hill Reps 75 min (5x3 min/ 6 reps"])
                        writer.writerow(["Thursday"])
                        writer.writerow(["Day off"])
                        writer.writerow(["Friday"])
                        writer.writerow(["Swim: 1,500m time trial"])
                        writer.writerow(["Cycling: Aerobic endurance intervals 120 min"])
                        writer.writerow(["Run: transition immediately after bike 20 min"])
                        writer.writerow(["Saturday"])
                        writer.writerow(["Run: Aerobic Endurance 90 min"])
                        writer.writerow(["Cycling: Easy 30 min"])
                        writer.writerow(["Sunday"])
                        writer.writerow(["Day off"])
                        """
                        Functions used to generate csv rows
                        """
            elif self.radioButton_3.isChecked():
                """
                Method used to check if RadioButton_3 is selected when the submit button is clicked
                """
                with open('workout_plan.csv', 'w', newline='') as file:
                    """
                    Method used to generate a csv file based on int values from text input in the UI in the get
                    """
                    writer = csv.writer(file)
                    writer.writerow(["Week 1"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .6), " x 5 ", int(bench * .65), " x 5 ", int(bench * .7),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .35), " x 5", int(bench * .4), " x 5",
                         int(bench * .425),
                         " x 5"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .45), " x 6 ", int(bench * .55), " x 5 ", int(bench * .6),
                         " x 5 "])
                    writer.writerow(["3 sets of 8 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["5 Minutes Speed Bag"])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .6), " x 5 ", int(squat * .65), " x 5 ", int(squat * .7), " x 4 ",
                         int(squat * .75), " x 3 ", int(squat * .75), " x 3 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .25), " x 5 ", int(squat * .3), " x 5 ",
                                     int(squat * .325), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 5 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 6 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 6"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Big Boxing Bag"])
                    if bmi > 30:
                        writer.writerow(["5 Minutes"])
                    else:
                        writer.writerow(["10 Minutes"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .7),
                         " x 6 ", int(bench * .75), " x 6 ", int(bench * .75), " x 6 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .35), " x 5 ", int(bench * .4), " x 5 ", int(bench * .45),
                         " x 5 "])
                    writer.writerow(
                        ["1 dumbbell Military Press ", int(bench * .25), " x 5 ", int(bench * .3), " x 5 ",
                         int(bench * .35),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 8 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["5 Speed Bag"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .35), " x 5 ", int(clean * .4), " x 5 ", int(clean * .45),
                         " x 5 "])
                    writer.writerow(
                        ["Front Squat ", int(squat * .4), " x 7 ", int(squat * .46), " x 5 ", int(squat * .5), " x 5 "])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 4 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Body Bag Boxing"])
                    if bmi > 30:
                        writer.writerow(["10 Minutes"])
                    else:
                        writer.writerow(["5 Minutes"])

                    writer.writerow(["Week 2"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .65), " x 5 ", int(bench * .7), " x 5 ", int(bench * .75),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .4), " x 5", int(bench * .425), " x 5",
                         int(bench * .475),
                         " x 5"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .5), " x 6 ", int(bench * .6), " x 5 ", int(bench * .65),
                         " x 5 "])
                    writer.writerow(["3 sets of 8 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["5 Minutes Speed Bag"])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .65), " x 5 ", int(squat * .7), " x 5 ", int(squat * .75), " x 4 ",
                         int(squat * .8), " x 3 ", int(squat * .8), " x 3 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .3), " x 5 ", int(squat * .35), " x 5 ",
                                     int(squat * .375), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 5 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 6 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 6"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Big Boxing Bag"])
                    if bmi > 30:
                        writer.writerow(["5 Minutes"])
                    else:
                        writer.writerow(["10 Minutes"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .55), " x 8 ", int(bench * .65), " x 8 ", int(bench * .75),
                         " x 6 ", int(bench * .8), " x 6 ", int(bench * .8), " x 6 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .4), " x 5 ", int(bench * .45), " x 5 ", int(bench * .5),
                         " x 5 "])
                    writer.writerow(
                        ["1 dumbbell Military Press ", int(bench * .3), " x 5 ", int(bench * .35), " x 5 ",
                         int(bench * .4),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 8 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["5 Speed Bag"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .4), " x 5 ", int(clean * .45), " x 5 ", int(clean * .5),
                         " x 5 "])
                    writer.writerow(
                        ["Front Squat ", int(squat * .45), " x 7 ", int(squat * .5), " x 5 ", int(squat * .55),
                         " x 5 "])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 4 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Body Bag Boxing"])
                    if bmi > 30:
                        writer.writerow(["10 Minutes"])
                    else:
                        writer.writerow(["5 Minutes"])

                    writer.writerow(["Week 3"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .7), " x 5 ", int(bench * .75), " x 5 ", int(bench * .8),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .45), " x 5", int(bench * .5), " x 5",
                         int(bench * .525),
                         " x 5"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .55), " x 6 ", int(bench * .65), " x 5 ", int(bench * .7),
                         " x 5 "])
                    writer.writerow(["3 sets of 8 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["5 Minutes Speed Bag"])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .7), " x 5 ", int(squat * .75), " x 5 ", int(squat * .8), " x 4 ",
                         int(squat * .85), " x 3 ", int(squat * .85), " x 3 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .35), " x 5 ", int(squat * .4), " x 5 ",
                                     int(squat * .425), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 5 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 6 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 6"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Big Boxing Bag"])
                    if bmi > 30:
                        writer.writerow(["5 Minutes"])
                    else:
                        writer.writerow(["10 Minutes"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .6), " x 8 ", int(bench * .7), " x 8 ", int(bench * .8),
                         " x 6 ", int(bench * .85), " x 6 ", int(bench * .85), " x 6 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .45), " x 5 ", int(bench * .5), " x 5 ", int(bench * .55),
                         " x 5 "])
                    writer.writerow(
                        ["1 dumbbell Military Press ", int(bench * .35), " x 5 ", int(bench * .4), " x 5 ",
                         int(bench * .45),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 8 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["5 Speed Bag"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .45), " x 5 ", int(clean * .5), " x 5 ", int(clean * .55),
                         " x 5 "])
                    writer.writerow(
                        ["Front Squat ", int(squat * .5), " x 7 ", int(squat * .56), " x 5 ", int(squat * .6), " x 5 "])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 4 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Body Bag Boxing"])
                    if bmi > 30:
                        writer.writerow(["10 Minutes"])
                    else:
                        writer.writerow(["5 Minutes"])

                    writer.writerow(["Week 4"])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .75), " x 5 ", int(bench * .8), " x 5 ", int(bench * .85),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .5), " x 5", int(bench * .525), " x 5",
                         int(bench * .575),
                         " x 5"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .6), " x 6 ", int(bench * .7), " x 5 ", int(bench * .75),
                         " x 5 "])
                    writer.writerow(["3 sets of 8 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["5 Minutes Speed Bag"])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .75), " x 5 ", int(squat * .8), " x 5 ", int(squat * .85), " x 4 ",
                         int(squat * .9), " x 3 ", int(squat * .9), " x 3 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .4), " x 5 ", int(squat * .45), " x 5 ",
                                     int(squat * .475), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 5 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 6 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 6"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Big Boxing Bag"])
                    if bmi > 30:
                        writer.writerow(["5 Minutes"])
                    else:
                        writer.writerow(["10 Minutes"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .65), " x 8 ", int(bench * .75), " x 8 ", int(bench * .85),
                         " x 6 ", int(bench * .9), " x 6 ", int(bench * .9), " x 6 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .5), " x 5 ", int(bench * .55), " x 5 ", int(bench * .6),
                         " x 5 "])
                    writer.writerow(
                        ["1 dumbbell Military Press ", int(bench * .4), " x 5 ", int(bench * .45), " x 5 ",
                         int(bench * .5),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 8 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["5 Speed Bag"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .5), " x 5 ", int(clean * .55), " x 5 ", int(clean * .6),
                         " x 5 "])
                    writer.writerow(
                        ["Front Squat ", int(squat * .55), " x 7 ", int(squat * .6), " x 5 ", int(squat * .65),
                         " x 5 "])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 4 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Body Bag Boxing"])
                    if bmi > 30:
                        writer.writerow(["10 Minutes"])
                    else:
                        writer.writerow(["5 Minutes"])

                    writer.writerow(["Week 5"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .8), " x 5 ", int(bench * .85), " x 5 ", int(bench * .9),
                         " x 5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .55), " x 5", int(bench * .6), " x 5",
                         int(bench * .625),
                         " x 5"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .65), " x 6 ", int(bench * .75), " x 5 ", int(bench * .8),
                         " x 5 "])
                    writer.writerow(["3 sets of 8 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["5 Minutes Speed Bag"])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .8), " x 5 ", int(squat * .85), " x 5 ", int(squat * .9), " x 4 ",
                         int(squat * .95), " x 3 ", int(squat * .95), " x 3 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .45), " x 5 ", int(squat * .5), " x 5 ",
                                     int(squat * .525), " x 5 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 5 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 6 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 6"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Big Boxing Bag"])
                    if bmi > 30:
                        writer.writerow(["5 Minutes"])
                    else:
                        writer.writerow(["10 Minutes"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .7), " x 8 ", int(bench * .8), " x 8 ", int(bench * .9),
                         " x 6 ", int(bench * .95), " x 6 ", int(bench * .95), " x 6 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .55), " x 5 ", int(bench * .6), " x 5 ", int(bench * .65),
                         " x 5 "])
                    writer.writerow(
                        ["1 dumbbell Military Press ", int(bench * .45), " x 5 ", int(bench * .5), " x 5 ",
                         int(bench * .55),
                         " x 5 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 8 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["5 Speed Bag"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .55), " x 5 ", int(clean * .6), " x 5 ", int(clean * .65),
                         " x 5 "])
                    writer.writerow(
                        ["Front Squat ", int(squat * .6), " x 7 ", int(squat * .66), " x 5 ", int(squat * .7), " x 5 "])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 4 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 8"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["Body Bag Boxing"])
                    if bmi > 30:
                        writer.writerow(["10 Minutes"])
                    else:
                        writer.writerow(["5 Minutes"])

                    writer.writerow(["Week 6"])
                    writer.writerow(["Monday"])
                    writer.writerow(
                        ["Hang power clean ", int(clean * .6), " x 8 ", int(clean * .7), " x 6 ",
                         int(clean * .8), " x 4 ", int(clean * .85), " x 4 ", int(clean * .85), " x 4 ",
                         int(clean * .9), " x 2 ", int(clean * .95), " x 2 ", int(clean), " x 1 "])
                    writer.writerow(
                        ["Incline Bench ", int(bench * .5), " x 8 ", int(bench * .6), " x 8 ", int(bench * .65),
                         " x 5 ", int(bench * .7), " x 5 ", int(bench * .75), " x 5 ", int(bench * .75),
                         " x 5 ", int(bench * .8),
                         " x 5 ", int(bench * .85),
                         " x 2-5 "])
                    writer.writerow(
                        ["DB bench, weight per dumbbell ", int(bench * .45), " x 8", int(bench * .5), " x 8",
                         int(bench * .55),
                         " x 8"])
                    writer.writerow(["Back extension ", " 5 ", "x 5 ", " 10 ", "x 5 ", " 15 ", "x 5 "])
                    writer.writerow(
                        ["Military press ", int(bench * .6), " x 8 ", int(bench * .65), " x 6-8 ", int(bench * .7),
                         " x 6-8 "])
                    writer.writerow(["3 sets of 10 lateral raise, choose dumbbell"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(
                        ["Build-ups 6 x 30", "rest 15 sec between reps", "Short sprints with resistance bands",
                         "rest 15 sec between reps", " 5x40 yards", "rest 15 sec between reps", ])
                    writer.writerow(["Tuesday"])
                    writer.writerow(
                        ["Back Squat ", int(squat * .6), " x 8 ", int(squat * .7), " x 6 ", int(squat * .8), " x 4 ",
                         int(squat * .85), " x 4 ", int(squat * .85), " x 4 ", int(squat * .9), " x 3 ",
                         int(squat * .95), " x 3 ",
                         int(squat), " x 2-4 "])
                    writer.writerow(["Bulgarian Split Squad ", int(squat * .55), " x 8 ", int(squat * .6), " x 8 ",
                                     int(squat * .65), " x 8 "])
                    writer.writerow(["3 sets of neutral grip pull up, 5-12 reps"])
                    writer.writerow(["3 sets of 1-dumbbell row any choice weight, 6 reps"])
                    writer.writerow(["3 sets of Leg Curl Machine any choice weight, 10 reps"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["6 x 110's 2 full gassers, 2 half gassers, 2 50 yars sprints, 1 minute rest"])
                    if bmi > 30:
                        writer.writerow(["20, 39, 18, 8 seconds to complete"])
                    else:
                        writer.writerow(["16, 34,15,5 seconds to complete"])
                    writer.writerow(["Thursday"])
                    writer.writerow(
                        ["Bench Press ", int(bench * .6), " x 8 ", int(bench * .7), " x 8 ", int(bench * .8),
                         " x 5 ", int(bench * .85), " x 5 ", int(bench * .9), " x 3 ",
                         int(bench * .95), " x 3 ", int(bench), " x 2-4 "])
                    writer.writerow(
                        ["1 dumbbell incline ", int(bench * .35), " x 8 ", int(bench * .4), " x 8 ", int(bench * .425),
                         " x 8 ", int(bench * .5),
                         " x 6 ", int(bench * .55),
                         " x 6 "])
                    writer.writerow(["3 sets of push-ups, as many as possible"])
                    writer.writerow(
                        ["1 dumbbell push press ", int(bench * .42), " x 8 ", int(bench * .47), " x 8 ",
                         int(bench * .5),
                         " x 8 "])
                    writer.writerow(["3 sets of bent over raise chose weight, 10 reps"])
                    writer.writerow(["Any triceps extension, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2 sets of L drill, 2 sets of Pro Agility, 5,10,15 yard ladder x 6"])
                    writer.writerow(["Friday"])
                    writer.writerow(
                        ["Hang High Pull ", int(clean * .35), " x 3 ", int(clean * .4), " x 3 ", int(clean * .425),
                         " x 3 ", int(clean * .45),
                         " x 3 ", int(clean * .5),
                         " x 3 ", int(clean * .55),
                         " x 3 ", int(clean * .6),
                         " x 2-3 "])
                    writer.writerow(["3 sets of 5 reps box jump with 20-30 inch box"])
                    writer.writerow(
                        ["Front Squat ", int(squat * .5), " x 7 ", int(squat * .56), " x 5 ", int(squat * .6), " x 3 ",
                         int(squat * .65), " x 3 ", int(squat * .7), " x 2 ", int(squat * .75), " x 2 "])
                    writer.writerow([
                        "Set up 4-6 hurdles. Side step over low hurdle, then step under high hurdle 3 times each direction"])
                    writer.writerow(["3 Sets of cross over step up, choose weight"])
                    writer.writerow(["3 sets of wide grip pull ups, 3-10 reps"])
                    writer.writerow(["3 Sets of single leg goblet squat, choose weight"])
                    writer.writerow(["3 Sets of seated row, choose weight"])
                    writer.writerow(["Any arm curl exercise, 3 sets of 12"])
                    writer.writerow(["Conditioning"])
                    writer.writerow(["2x300 yard shuttle, 5 min rest"])
                    if bmi > 30:
                        writer.writerow(["64 seconds to complete"])
                    else:
                        writer.writerow(["59 seconds to complete"])
                    """
                    Functions used to calculate and output rows to csv based on int values
                    """
        except ValueError:
            """
            Method used if values from text input in the UI are not Int
            """
            self.label_10.setText(
            "\t\tHeight, Weight, Bench, Squat, and Clean\n\t\tneed to be integers\n\t\te.g. 10, not 10.25 or ten and a quarter.\n\t\t Click clear to reset to default weights")
            """
            Functions used to change label text
            """

    def clear(self):
        """
        Method to create a button that will reset the UI to default parameters.
        :return: default UI parameters.
        """
        self.lineEdit.setText("")
        self.lineEdit_2.setText("")
        self.lineEdit_3.setText("45")
        self.lineEdit_4.setText("45")
        self.lineEdit_5.setText("45")
        self.label_10.setText("")
        self.radioButton.setChecked(False)
        self.radioButton_2.setChecked(False)
        self.radioButton_3.setChecked(False)
