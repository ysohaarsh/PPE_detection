
# PPE Detection using YOLO

![PPE Detection](ppe.jpg)

## Overview

This project demonstrates real-time personal protective equipment (PPE) detection using YOLO (You Only Look Once) object detection. It identifies and labels various PPE items in an input video stream or webcam feed, such as hardhats, masks, safety vests, machinery, and more.

The code is inspired by Murtaza's Workshop object detection tutorial and is implemented using the Ultralytics YOLO framework.

## Requirements

- Python 3.7+
- Ultralytics library (`pip install ultralytics`)
- OpenCV (`pip install opencv-python`)
- cvzone (`pip install cvzone`)

## Usage

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/ppe-detection.git
   ```

2. Open a terminal and navigate to the project directory:

   ```bash
   cd ppe-detection
   ```

3. Run the PPE detection script:

   ```bash
   python ppe_detection.py
   ```

   This will start the PPE detection application using your webcam as the video source. You can also modify the script to use a different video source (e.g., a video file).

## Custom Training (Optional)

If you want to train your own PPE detection model using custom data, you can follow these steps:

1. Collect and organize your dataset, and create a YAML file specifying the dataset's configuration.

2. Train the YOLO model with your custom data:

   ```bash
   !yolo task=detect mode=train model=yolov8l.pt conf=0.25 data="path/to/your/data.yaml" epochs=50 imgsz=640
   ```

3. Replace `"path/to/your/data.yaml"` with the path to your custom dataset's YAML file.

## Configuration

- The class names for detected objects can be customized in the `classNames` list within the script.
- You can adjust the confidence threshold for object detection by modifying the `conf` variable in the script.

## Credits

This project is inspired by Murtaza's Workshop object detection tutorial.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```

Please make sure to replace `"https://github.com/yourusername/ppe-detection.git"` with the actual URL of your GitHub repository, and customize other sections as needed, such as the usage instructions, dataset details, and license information.