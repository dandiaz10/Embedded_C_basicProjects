################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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
diazTenorio_Assignment4.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
diazTenorio_Assignment4.list \

OBJCOPY_BIN += \
diazTenorio_Assignment4.bin \


# All Target
all: diazTenorio_Assignment4.elf secondary-outputs

# Tool invocations
diazTenorio_Assignment4.elf: $(OBJS) $(USER_OBJS) C:\Users\Dann\STM32CubeIDE\workspace_1.2.0\diazTenorio_Assignment4\STM32L432KCUX_FLASH.ld
	arm-none-eabi-gcc -o "diazTenorio_Assignment4.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Dann\STM32CubeIDE\workspace_1.2.0\diazTenorio_Assignment4\STM32L432KCUX_FLASH.ld" --specs=nosys.specs -Wl,-Map="diazTenorio_Assignment4.map" -Wl,--gc-sections -static -u_printf_float -u_scanf_float --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

diazTenorio_Assignment4.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "diazTenorio_Assignment4.list"
	@echo 'Finished building: $@'
	@echo ' '

diazTenorio_Assignment4.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "diazTenorio_Assignment4.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
