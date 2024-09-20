ARCHS = arm64 
TARGET = iphone:13.7
FINALPACKAGE = 1
FOR_RELEASE = 1
THEOS_PACKAGE_SCHEME = rootless
include $(THEOS)/makefiles/common.mk

# FRAMEWORK_NAME = AWSS3
TWEAK_NAME = jailbreaklite

$(TWEAK_NAME)_FRAMEWORKS = UIKit Foundation Security QuartzCore CoreGraphics CoreText  AVFoundation Accelerate GLKit SystemConfiguration GameController
$(TWEAK_NAME)_LDFLAGS+= 
$(TWEAK_NAME)_CFLAGS = -fobjc-arc -Wno-deprecated-declarations -Wno-unused-variable -Wno-unused-value
#$(TWEAK_NAME)_OBJ_FILES = libdobby.a
$(TWEAK_NAME)_CCFLAGS = -std=c++11 -fno-rtti -fno-exceptions -DNDEBUG
$(TWEAK_NAME)_FILES = patch.mm

include $(THEOS_MAKE_PATH)/tweak.mk
# include $(THEOS_MAKE_PATH)/framework.mk