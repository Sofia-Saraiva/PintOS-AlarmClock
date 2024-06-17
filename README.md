# ⏰ PintOS Project: Solving Busy Wait with Alarm Clock

## 📄 Description

This project enhances PintOS by replacing busy wait loops with an alarm clock mechanism, reducing CPU usage and improving system efficiency by allowing processes to sleep until needed without consuming resources.

## 🛠 2.2.2 Alarm Clock

### 🔧 Modified Files and Functions
- **`threads/thread.c`**:
  - **Functions**:
    - `thread_init()` 
- **`devices/timer.c`**:
  - **Functions**:
    - `timer_sleep()`
    - `timer_interrupt()`
      
### 📐 Implementation Details
- **Data Structures**: Implemented an ordered list of timer events, each with an expiration time and a reference to the process to be awakened.
- **Functionality**: Added functions to initialize the alarm clock, add timer events, and handle expired events.
- **Scheduler Integration**: Modified the scheduler to integrate with the new alarm clock mechanism.

## 🧪 Testing on Pint-OS after compiling the code with changes
   ```bash
   pintos -- -q run alarm-multiple
   ```

## 📜 License

This project is licensed under the [MIT License](LICENSE).
