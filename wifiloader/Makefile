LOCAL_PATH := $(call my-dir)

LOCAL_SRC_FILES := \
    wifiloader.c

LOCAL_SHARED_LIBRARIES := \
    libcutils liblog libutils

ifneq ($(WIFI_DRIVER_MODULE_NAME),)
LOCAL_CFLAGS += -DWIFI_DRIVER_MODULE_NAME=\"$(WIFI_DRIVER_MODULE_NAME)\"
endif

ifneq ($(WIFI_DRIVER_MODULE_PATH),)
LOCAL_CFLAGS += -DWIFI_DRIVER_MODULE_PATH=\"$(WIFI_DRIVER_MODULE_PATH)\"
endif

ifneq ($(WIFI_DRIVER_FW_PATH_PARAM),)
LOCAL_CFLAGS += -DWIFI_DRIVER_FW_PATH_PARAM=\"$(WIFI_DRIVER_FW_PATH_PARAM)\"
endif

LOCAL_MODULE := wifiloader

all:
    gcc -g -wall $LOCAL_CFLAGS -o wifiloader $LOCAL_SRC_FILES libutil.so liblog.so libcutil.so