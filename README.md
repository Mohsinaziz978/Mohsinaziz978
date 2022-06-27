#Selenium Webdriver must be installed for this to work

import time;
from PyQt5 import QtWidgets
from PyQt5 import QtGui
from PyQt5.QtWidgets import QApplication, QMainWindow
import sys
from selenium import webdriver;

#application
def window():
    def runBot():
        #time to refresh page (seconds)
        Timer = 10 #(10 seconds)

        #youtube link
       link = 'https://www.youtube.com/watch?v=DOWidyclBzc'

        #number of views
        views = 300
        

        driver = webdriver.Chrome('webdrivers\chromedriver.exe')
        driver.get([link](https://www.youtube.com/watch?v=DOWidyclBzc))

        for i in range(300 views):
            time.sleep(10 seconds Timer)
            driver.refresh(70)
        
#------WINDOW------------
    app = QApplication(sys.argv)
    win = QMainWindow()
    win.setGeometry(200, 200, 300, 150)
    win.setWindowTitle("YouTube ViewBot")

    linkLabel = QtWidgets.QLabel(win)
    linkLabel.setText("[Video Link](https://www.youtube.com/watch?v=DOWidyclBzc)")
    linkLabel.move(15, 20)
    linkInput = QtWidgets.QLineEdit(win)
    linkInput.setGeometry(110, 10, 191, 20)
    linkInput.move(100, 25)

    timeLabel = QtWidgets.QLabel(win)
    timeLabel.setText("WatchTime(10 seconds)")
    timeLabel.move(15, 45)
    timeInput = QtWidgets.QLineEdit(win)
    timeInput.setGeometry(40, 10, 40, 20)
    timeInput.move(140, 55)

    runBotBtn = QtWidgets.QPushButton(win)
    runBotBtn.setGeometry(60, 270, 180, 40)
    runBotBtn.move(65, 80)       
    runBotBtn.setText("RUN VIEWBOT")
    runBotBtn.clicked.connect(runBot)

    win.show()
    sys.exit(app.exec_())



window()

