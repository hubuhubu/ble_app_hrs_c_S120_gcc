TARGET_CHIP := NRF51822_QFAA_CA
BOARD := BOARD_NRF6310


C_SOURCE_FILES += main.c
C_SOURCE_FILES += ble_hrs_c.c
C_SOURCE_FILES += ble_bas_c.c

C_SOURCE_FILES += ble_db_discovery.c
C_SOURCE_FILES += simple_uart.c

C_SOURCE_FILES += nRF6350.c
C_SOURCE_FILES += twi_hw_master.c
C_SOURCE_FILES += pstorage.c
C_SOURCE_FILES += device_manager_central.c
C_SOURCE_FILES += app_button.c
C_SOURCE_FILES += app_gpiote.c
C_SOURCE_FILES += app_timer.c
C_SOURCE_FILES += softdevice_handler.c
C_SOURCE_FILES += ble_debug_assert_handler.c
C_SOURCE_FILES += app_trace.c

SDK_PATH = ../../../../../../

INCLUDEPATHS += -I"$(SDK_PATH)Include/app_common"
INCLUDEPATHS += -I"$(SDK_PATH)Include"
INCLUDEPATHS += -I"$(SDK_PATH)Include/ble"
INCLUDEPATHS += -I"$(SDK_PATH)Include/ble/device_manager"
INCLUDEPATHS += -I"$(SDK_PATH)Include/s120"
INCLUDEPATHS += -I"$(SDK_PATH)Include/ble/ble_services"
INCLUDEPATHS += -I"$(SDK_PATH)Include/boards"
INCLUDEPATHS += -I"$(SDK_PATH)Include/sd_common"
INCLUDEPATHS += -I"../../common"

INCLUDEPATHS += -I"../../../experimental"

INCLUDEPATHS += -I"$(SDK_PATH)Include/ext_sensors"
INCLUDEPATHS += -I"$(SDK_PATH)Include/sdk"
C_SOURCE_PATHS += ../../common/
C_SOURCE_PATHS += $(SDK_PATH)Source/ble/device_manager/experimental/
C_SOURCE_PATHS +=$(SDK_PATH)Source/simple_uart/
C_SOURCE_PATHS +=$(SDK_PATH)Source/ext_sensors/nRF6350/
C_SOURCE_PATHS +=$(SDK_PATH)Source/twi_master/
C_SOURCE_PATHS +=$(SDK_PATH)Source/app_common/
C_SOURCE_PATHS +=$(SDK_PATH)Source/ble/device_manager/experimental/
C_SOURCE_PATHS +=$(SDK_PATH)Source/sd_common/
C_SOURCE_PATHS +=$(SDK_PATH)Source/ble/
CFLAGS := -DDEBUG_NRF_USER -DBLE_STACK_SUPPORT_REQD -DS120
OUTPUT_FILENAME := ble_hrs_c_gcc

CFLAGS += -ffunction-sections

DEVICE_VARIANT := xxaa
#DEVICE_VARIANT := xxab

USE_SOFTDEVICE := S120
#USE_SOFTDEVICE := s210

include $(SDK_PATH)Source/templates/gcc/Makefile.common
