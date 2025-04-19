# Boot-Loader-Simlation
Boot Loader Simlation Descripition
#include <stdio.h> 
#include <unistd.h>  
void bios() { 
printf("BIOS: Initializing hardware...\n"); 
sleep(1); 
printf("BIOS: POST (Power-On Self Test) completed.\n\n"); 
} 
void loadBootloader() { 
printf("Bootloader: Loading bootloader into memory...\n"); 
sleep(1); 
printf("Bootloader: Bootloader ready.\n\n"); 
} 
void loadKernel() { 
printf("Bootloader: Loading OS Kernel...\n"); 
for(int i = 0; i <= 100; i += 25) { 
printf("   Loading... %d%%\n", i); 
sleep(1); 
} 
BOOT LOADER SIMULATION      
OPERATING SYSTEMS 
printf("Bootloader: Kernel successfully loaded.\n\n"); 
} 
void startOS() { 
printf("Kernel: Starting the Operating System...\n"); 
sleep(1); 
printf("OS is now running! Welcome!\n"); 
} 
int main() { 
printf("Power ON\n\n"); 
bios(); 
loadBootloader(); 
loadKernel(); 
startOS(); 
return 0; 
}
