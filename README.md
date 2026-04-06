# HKU Tam Wing Fan Innovation Wing's 3D Motion Capture System — README

## Overview

This github repo provides a complete workflow for operating **3D Optical Motion Capture System** in Event Hall B using **Vicon Nexus 2.16**. It covers system calibration, subject setup, motion capture, and data export.

This guide is intended for students, researchers, and lab users working in the HKU Faculty of Engineering Motion Capture Lab.

---

## System Information

* **System Name:** 3D Optical Motion Capture System
* **Software:** Vicon Nexus 2.16
* **Location:** Event Hall B
* **Version:** 0.10 (Last updated: 02 April 2026)

### Equipment & Accessories

* Active Wand
* Reflective markers (hard & soft)
* Marker suit
* X-base markers
* Dummy model

---

## Workflow Summary

The motion capture process consists of three main stages:

1. **Calibration**
2. **Data Capture**
3. **View & Export**

---

## 1. Calibration

Calibration ensures accurate tracking of markers and proper spatial alignment.

### Steps:

1. **Start System**

   * Open Vicon Nexus
   * Click **"Go Live"**

2. **Video Calibration Setup**

   * Select all cameras
   * Place active wand in view
   * Adjust threshold (0.2–0.5 if needed)
   * Ensure all calibration points are detected

3. **Mask Cameras**

   * Remove reflective objects
   * Mask unwanted reflections (auto or manual)

4. **Calibrate Cameras**

   * Wave the calibration wand across the capture volume
   * Wait until all cameras turn green

5. **Set Floor Origin & Plane**

   * Place wand at center for origin
   * Use 6 markers to define floor plane

6. **Save Calibration**

   * Save calibration file for reuse
   * Recommended path: `D:\Motion Capture\xcp saves`

---

## 2. Data Capture

### 2.1 Database Management

* Create database
* Define subject classification
* Create:
  
  * Patient
  * Session
  * Select session before proceeding

---

### 2.2 Create Subject

* Select a **VSK (Vicon Skeleton)** (e.g., Plug-in Gait Lower Body)
* Input required subject data
* Save subject

---

### 2.3 Marker Placement

* Use appropriate marker template (e.g., Plug-in Gait)
* Attach markers precisely on joints
* Ensure correct suit positioning

---

### 2.4 Capturing Motion

#### Static Trial

* Stand still in **motorbike pose**
* Capture for ~5 seconds

**Processing:**

1. Reconstruct markers
2. Auto-initialize skeleton
3. Run Plug-in Gait Static pipeline

---

#### Dynamic Trial

* Start capture (manual or trigger-based)
* Perform movement (e.g., walking)

**Processing:**

1. Reconstruct and label markers
2. Check data quality
3. Fix gaps:
   * Fill gaps OR
   * Trim timeline
4. Run Plug-in Gait Dynamic pipeline

---

## 3. View & Export

* Review captured motion data
* Export results for analysis or further processing

---

## Best Practices

* Always **save calibration files**
* Ensure **clear capture volume** (no reflections)
* Verify **marker placement accuracy**
* Check for **data gaps** before exporting
* Maintain organized **database structure**

---

## Contact

For questions or support:

* Tam Wing Fan Innovation Wing Techinicians
* Motion Capture Team
* Email: [ehank2142@connect.hku.hk](mailto:ehank2142@connect.hku.hk)

---

## Notes

* This system is sensitive to lighting and reflections
* Calibration quality directly impacts data accuracy
* Proper setup significantly reduces post-processing time

---

## License / Usage

This system and guide are intended for educational and research use within HKU.

---
