################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include subdir.mk
-include arduino/core/avr-libc/subdir.mk
-include arduino/core/subdir.mk
-include Libraries/Wire/utility/subdir.mk
-include Libraries/Wire/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(CC_DEPS)),)
-include $(CC_DEPS)
endif
ifneq ($(strip $(C++_DEPS)),)
-include $(C++_DEPS)
endif
ifneq ($(strip $(C_UPPER_DEPS)),)
-include $(C_UPPER_DEPS)
endif
ifneq ($(strip $(CXX_DEPS)),)
-include $(CXX_DEPS)
endif
ifneq ($(strip $(CPP_DEPS)),)
-include $(CPP_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
AR += \
/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/arduino.ar \

ELF += \
HerculesRemoteControl.elf \

EEP += \
HerculesRemoteControl.eep \

FLASH_IMAGE += \
HerculesRemoteControl.hex \


# All Target
all: HerculesRemoteControl

# Tool invocations
HerculesRemoteControl: $(FLASH_IMAGE)
	@echo 'Building target: $@'
	@echo 'Printing size:'
	"/home/alexandre/Desktop/eclipseArduino/arduino-1.5.6-r2/hardware/tools/avr/bin/avr-size" -A "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/HerculesRemoteControl.elf"
	@echo 'Finished building target: $@'
	@echo ' '

/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/arduino.ar: $(AR_OBJ)
	@echo 'Starting archiver'
	"/home/alexandre/Desktop/eclipseArduino/arduino-1.5.6-r2/hardware/tools/avr/bin/avr-ar" rcs "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/arduino.ar"   $(AR_OBJ)
	@echo 'Finished building: $@'
	@echo ' '

HerculesRemoteControl.elf: $(LINK_OBJ) $(AR)
	@echo 'Starting combiner'
	"/home/alexandre/Desktop/eclipseArduino/arduino-1.5.6-r2/hardware/tools/avr/bin/avr-gcc" -Os -Wl,--gc-sections -mmcu=atmega328p -o "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/HerculesRemoteControl.elf"   $(LINK_OBJ) $(AR)  "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/arduino.ar" "-L/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release" -lm
	@echo 'Finished building: $@'
	@echo ' '

HerculesRemoteControl.eep: $(ELF)
	@echo 'Create eeprom image'
	"/home/alexandre/Desktop/eclipseArduino/arduino-1.5.6-r2/hardware/tools/avr/bin/avr-objcopy" -O ihex -j .eeprom --set-section-flags=.eeprom=alloc,load --no-change-warnings --change-section-lma .eeprom=0 "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/HerculesRemoteControl.elf" "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/HerculesRemoteControl.eep"
	@echo 'Finished building: $@'
	@echo ' '

HerculesRemoteControl.hex: $(EEP)
	@echo 'Create Flash image (ihex format)'
	"/home/alexandre/Desktop/eclipseArduino/arduino-1.5.6-r2/hardware/tools/avr/bin/avr-objcopy" -O ihex -R .eeprom "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/HerculesRemoteControl.elf" "/home/alexandre/Desktop/workspace/HerculesRemoteControl/Release/HerculesRemoteControl.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(C_UPPER_DEPS)$(C_DEPS)$(AR)$(EEP)$(FLASH_IMAGE)$(CC_DEPS)$(AR_OBJ)$(C++_DEPS)$(LINK_OBJ)$(CXX_DEPS)$(SIZEDUMMY)$(ELF)$(CPP_DEPS) HerculesRemoteControl
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
