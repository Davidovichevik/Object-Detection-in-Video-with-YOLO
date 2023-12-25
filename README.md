# Object-Detection-in-Video-with-YOLO
Object detection in a video using the YOLO (You Only Look Once) model
import cv2
import numpy as np

net = cv2.dnn.readNet('yolov3.weights', 'yolov3.cfg')
layer_names = net.getUnconnectedOutLayersNames()

cap = cv2.VideoCapture('video.mp4')

while True:
    ret, frame = cap.read()

    # Implement YOLO object detection logic

    cv2.imshow('Object Detection', frame)

    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
