


# 🔷 PE-Backdooring

 - This Repository Will Teach You How You Can Backdoor Any PE File 
 - How You Can Convert Simple PE into a reverse shell
 -  How You Can Craft Trojans With Shellcode
---

## 🔷 My Introduction
Hi my name is Aryan, im a cyber security student, just a 17 year old kid who loves Hacking and Programming, i love RE | Malware Dev and Analysis | Game Hacking etc. 


## 🧪 Introduction to PE-Backdooring 

**What is PE** - *PE is (Portable Executable) an executable file format which you typically see in windows .exe .dll .scr*
**What is Backdoor** - *Backdoor or backdooring is a method used for getting unauthorized access to any computer. Basically You can control someones computer from your computer without them knowing about it.*

So Basic idea of this repo is to make you understand how any hacker can plant a backdoor in your daily use softwares, So if for example you play **Call Of Duty Warzone** every day or any other game like **Battlefield 6** 
hacker can convert your game's exe to a malware can hack you.
And also this is **how people get hacked when they download crack software or games**.

---

## ▶️ Video Explanation ( if you want)
I have explained everything on my **Youtube Channel**  [Watch Video!](https://youtu.be/SH95uXG-RXY?si=vdffzp9UJllloRAZ)

---

## 🔰 Generating a PE for Testing
Ok Now First we need a PE file to experiment on right? 

i made a simple messagebox program in C++ which we will backdoor
think of it like its a **Photoshop 2025 software**

---
CODE:

    #include<Windows.h>
    
    int main(){
	    MessageBoxW(NULL,L"Photoshop.exe",L"Photoshop is now running",MB_OK);
	    return 0;
	   }

---
**Output of this program**:


<img width="240" height="170" alt="Screenshot 2025-08-20 205019" src="https://github.com/user-attachments/assets/52b5c10a-b347-4d46-95b8-f58680b8bdb9" />

## ☠️ Generating A Shellcode(Malware)

Now we will make our payload basiclly with will give us the shell
but right now for testing we will make a shellcode to open calculator in windows


### Step 1: Open msfconsole in kali linux or any other distro

### Step 2: 
---
COMMAND:

 	//Opens msfconsole
	msfconsole

  	//Mention payload as Shellcode
  	use payload/windows/exec

 	//Set command with will execute
   	set CMD calc.exe

	//generate shellcode
 	generate -f raw -o shellocde.bin

---

### Step 3: Download this bin file to your windows machine



