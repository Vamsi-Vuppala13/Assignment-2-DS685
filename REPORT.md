# Run Report — Assignment 2

## Pipeline Summary

This report summarizes the execution results for Robotics Assignment 2. The simulation pipeline was started successfully, and the detection/ingestion workflow was tested using the TurtleBot simulation environment.

## Run Details

| Item | Value |
|---|---|
| Total events ingested | 73 |
| Total detections | 0 |
| Robot ID | `tb3_sim` |
| ROS Distribution | `jazzy` |

## Class Histogram

No object classes were detected during this run.

The simulation used geometric placeholder objects for the world assets. Because these objects were simple shapes instead of realistic textured objects, the detector did not classify them as valid objects during the test run.

## System Components

| Component | Tool |
|---|---|
| Detector | YOLOv8n using Ultralytics |
| Transport | Eclipse Zenoh |
| Database | PostgreSQL 15 |
| Robot Platform | TurtleBot simulation |
| ROS Distribution | ROS 2 Jazzy |

## Detection Event Topic Pattern

The detection events followed the required Zenoh key structure:

```text
maze/<robot_id>/<run_id>/detections/v1/<event_id>
