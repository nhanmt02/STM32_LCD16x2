################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
LCD16X2_GPIO.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
LCD16X2_GPIO.list \

OBJCOPY_HEX += \
LCD16X2_GPIO.hex \

OBJCOPY_BIN += \
LCD16X2_GPIO.bin \


# All Target
all: LCD16X2_GPIO.elf secondary-outputs

# Tool invocations
LCD16X2_GPIO.elf: $(OBJS) $(USER_OBJS) E:\Embedded_Workspace_k2\LCD16X2_GPIO\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "LCD16X2_GPIO.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\Embedded_Workspace_k2\LCD16X2_GPIO\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="LCD16X2_GPIO.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

LCD16X2_GPIO.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "LCD16X2_GPIO.list"
	@echo 'Finished building: $@'
	@echo ' '

LCD16X2_GPIO.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "LCD16X2_GPIO.hex"
	@echo 'Finished building: $@'
	@echo ' '

LCD16X2_GPIO.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "LCD16X2_GPIO.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
