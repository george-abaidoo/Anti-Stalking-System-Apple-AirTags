# 🛡️ Anti-Stalking System for Apple AirTags  

This repository showcases my Master's dissertation project: **Design and Development of an Anti-Stalking System for AirTags**.  
The project addresses the growing privacy and safety concerns surrounding Apple's AirTag tracking device, which, while useful for finding personal items, has also been misused for malicious stalking.  

---

## 🎯 Project Motivation
Apple AirTags leverage the **Find My network** and **Bluetooth Low Energy (BLE)** technology to track items. However, their small size and powerful tracking capabilities make them attractive tools for stalkers.  
Apple introduced some anti-stalking measures, but these are often:
- **Unreliable** (alerts on iPhone are inconsistent)  
- **Delayed** (AirTag sounds may take 8–24 hours)  
- **Manual** (Android users must scan with the Tracker Detect app, which only scans briefly)  

This project aimed to design a **more reliable and automatic detection system** to protect potential victims.  

---

## 🔬 Key Contributions
1. **Derived an Identifying Token**  
   - From the BLE advertising packets of AirTags, which was the Manufacturer Specific Data (MSD)  
   - This token can uniquely and reliably identify an AirTag among other BLE devices.  

2. **Android Application**  
   - Implemented a lightweight mobile app capable of scanning continuously for AirTags.  
   - Integrated real-time **alert notifications** when a suspicious AirTag is detected nearby.  

3. **Distance Estimation**  
   - Used **RSSI analysis** and a **Linear Regression model** to estimate the distance of the AirTag from the user.  
   - Provided an approximate location awareness in addition to detection.  

4. **Accuracy & Performance**  
   - Achieved **99.17% detection accuracy**.  
   - High precision (0.992) and very low false positive rate (0.008).  
   - Demonstrated superior performance compared to Apple’s Tracker Detect app.  

---

## 🛠️ Technical Overview
- **Platform:** Android  
- **Core Technology:** Bluetooth Low Energy (BLE) scanning  
- **Libraries/Tools:** Android BLE API, Python (NumPy, scikit-learn, statsmodels) for signal modeling  
- **Machine Learning:** Linear Regression model for signal strength prediction (Measured Power at 1m)  

---

## 📊 Experimental Results
- **True Positives & Negatives:** Correctly identified AirTags in range and excluded other BLE devices.  
- **Distance Estimation:** Provided reasonable approximations of how close/far an AirTag was.  
- **Alert System:** Immediate high-priority notifications within ~1 minute of detection.  

---

## 🚀 Future Work
- Extend implementation to **iOS devices**.  
- Explore **Polynomial Regression** or advanced ML models for more accurate distance estimation.  
- Improve detection of AirTags in **connected mode** (currently undetectable via BLE).  
- Broader validation using a larger dataset of BLE devices.  

---

## 📖 Dissertation
This project was completed as part of my **MSc in Cybersecurity**.  
Full dissertation: *Design and Development of an Anti-Stalking System for AirTags*.  

---

## 👨‍💻 Author
**George Abaidoo**  
- 🎓 MSc in Cybersecurity  
- 🔒 Interests: Cybersecurity, AI, BLE security, Mobile Application Development  
