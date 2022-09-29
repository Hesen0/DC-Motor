# DC-Motor
import time

from  pyfirmata import  Arduino
from time import sleep


port = 'COM5'
board = Arduino(port)

while True:
    board.digital[13].write(1)
    time.sleep(2)
    board.digital[13].write(0)
    time.sleep(2)
    board.digital[13].write(0)
    
