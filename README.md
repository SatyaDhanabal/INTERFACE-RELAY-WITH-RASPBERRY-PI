# INTERFACE-RELAY-WITH-RASPBERRY-PI
RELAY PROGRAM:
import RPi.GPIO as GPIO
import time
GPIO.setwarnings(False)
GPIO.setmode(GPIO.BOARD)
GPIO.setup(36, GPIO.OUT)
GPIO.setup(38, GPIO.OUT)
GPIO.setup(32, GPIO.OUT)
try:
 while True:
 GPIO.output(36, 1)
 print ("Relay1 ON")
 time.sleep(2)
 GPIO.output(38, 1)
 print ("Relay2 ON")
 time.sleep(2)
 GPIO.output(32, 1)
 print ("Relay3 ON")
 time.sleep(2)
 GPIO.output(36, 0)
 print ("Relay1 OFF")
 time.sleep(2)
 GPIO.output(38, 0)
 print ("Relay2 OFF")
 time.sleep(2)
 GPIO.output(32, 0)
 print ("Relay3 OFF")
 time.sleep(2)
except KeyboardInterrupt:
 GPIO.output(36, 0)
 GPIO.output(38, 0)
 GPIO.output(32, 0)
