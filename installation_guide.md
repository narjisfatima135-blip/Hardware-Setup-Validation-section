# Installation and Setup
This section explains how to install required drivers and run the VSDSquadron PRO board using Freedom Studio.

---

## 1. Install Drivers

### Step 1: Download Zadig
Download Zadig tool from:
https://zadig.akeo.ie/

### Step 2: Install Driver
1. Open Zadig
2. Go to **Options → List All Devices**
3. Select: Dual RS-232-HS (Interface 0)
4. Choose driver: libusb-win32
5. Click: Install / Reinstall Driver

---

## 2. Extract Freedom Studio

1. Right-click on downloaded file (VSDSquadronPRO.tar.gz)
2. Click **Extract here**
3. Open extracted folder

---

## 3. Launch Freedom Studio

1. Open Freedom Studio
2. Select workspace folder (example: D:\projects)
3. Click **Launch**

---

## 4. Create New Project

1. Go to:
File → New → SiFive Project
2. Select:
sifive-hifive1 target
3. Choose example:
sifive-welcome
4. Click Finish

---

## 5. Debug Configuration

1. Click **Debug**
2. Open Debug Configurations
3. Go to OpenOCD tab
4. Click Debug

---

## 6. Run Program

1. After debug window opens
2. Click **Run**
3. Program will execute on board
