# Commands Used for Build and Flash

This section documents all commands used during the setup, build, and execution of the program on VSD Squadron PRO board.

---

## 1. Build Process

- Build the project using Freedom Studio:
- Click on **Build Project** or press:
Ctrl + B

---

## 2. Debug and Run

- Click on **Debug** to start debugging session
- Select **OpenOCD** configuration
- Click **Debug**

---

## 3. Run Program

- After debugging starts:
- Click on **Run** button

---

## 4. Terminal Commands (if used)

```bash
# Navigate to project folder
cd project_directory

# Example build command
make

# Run output file
./output_file

## 5. Flashing to Board

- Connect VSD Squadron PRO board using USB cable
- Ensure drivers are installed using Zadig tool
- Open Freedom Studio

### Steps:
1. Click on **Debug**
2. Select **OpenOCD Configuration**
3. Click **Debug**
4. The program will be automatically flashed to the board

### Verification:
- Check console output
- Program executes successfully on hardware

