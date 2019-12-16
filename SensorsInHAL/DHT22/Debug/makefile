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
TempSensorNew.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
TempSensorNew.list \

OBJCOPY_HEX += \
TempSensorNew.hex \

OBJCOPY_BIN += \
TempSensorNew.bin \


# All Target
all: TempSensorNew.elf secondary-outputs

# Tool invocations
TempSensorNew.elf: $(OBJS) $(USER_OBJS) F:\Projects\cubeide\TempSensorNew\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "TempSensorNew.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"F:\Projects\cubeide\TempSensorNew\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="TempSensorNew.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

TempSensorNew.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "TempSensorNew.list"
	@echo 'Finished building: $@'
	@echo ' '

TempSensorNew.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "TempSensorNew.hex"
	@echo 'Finished building: $@'
	@echo ' '

TempSensorNew.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "TempSensorNew.bin"
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
