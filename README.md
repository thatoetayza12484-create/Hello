#ml.py
import time
import os

# Colors
CYAN = "\033[96m"
MAGENTA = "\033[95m"
YELLOW = "\033[93m"
GREEN = "\033[92m"
RED = "\033[91m"
BLUE = "\033[94m"
WHITE = "\033[97m"
RESET = "\033[0m"


def clear():
    os.system("cls" if os.name == "nt" else "clear")


def typing(text, color=WHITE, speed=0.04):
    for char in text:
        print(color + char + RESET, end="", flush=True)
        time.sleep(speed)
    print()


clear()

print(CYAN + "╔══════════════════════════════╗")
print(CYAN + "║       ✦  HELLO  ✦           ║")
print(CYAN + "╚══════════════════════════════╝" + RESET)

typing("Initializing...", YELLOW)
time.sleep(0.5)

typing("Loading...", GREEN)
time.sleep(0.5)

typing("Finding someone special...", MAGENTA)
time.sleep(1)

clear()

print(CYAN + "╔══════════════════════════════╗")
print(CYAN + "║       CHOOSE ONE 💫         ║")
print(CYAN + "╚══════════════════════════════╝" + RESET)

print()
print(MAGENTA + "[1] 🎵 Music")
print(BLUE + "[2] ☕ Coffee")
print(YELLOW + "[3] 🌙 Night Walk")
print(RED + "[4] ❤️ Something else")

choice = input(WHITE + "\nYour choice → " + RESET)

clear()

if choice == "1":
    typing("Good choice 🎵", MAGENTA)
    typing("But talking with you would be better.", CYAN)

elif choice == "2":
    typing("Coffee it is ☕", YELLOW)
    typing("You bring the smile.", MAGENTA)

elif choice == "3":
    typing("A night walk sounds nice 🌙", BLUE)
    typing("Especially with the right person.", CYAN)

elif choice == "4":
    typing("Interesting choice... 👀", RED)
    typing("Maybe I already know my choice.", MAGENTA)

else:
    typing("Hmm... not on the list 😭", RED)

print()
typing("SYSTEM MESSAGE: You're kinda special. ✨", CYAN)

input("\nPress ENTER to exit...")
