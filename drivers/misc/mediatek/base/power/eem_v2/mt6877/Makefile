
# Copyright (C) 2016 MediaTek Inc.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 2 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#-I$(srctree)/drivers/misc/mediatek/base/power/eem_v2/$(CONFIG_MTK_PLATFORM)/inc/	\
#-I$(srctree)/drivers/misc/mediatek/pmic/include/	\
#

ccflags-y += \
	-I$(srctree)/drivers/misc/mediatek/base/power/include/spm_v3/	\
	-I$(srctree)/drivers/misc/mediatek/base/power/$(CONFIG_MTK_PLATFORM)\
	-I$(srctree)/drivers/misc/mediatek/base/power/include/	\
	-I$(srctree)/drivers/misc/mediatek/include/mt-plat/	\
	-I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(CONFIG_MTK_PLATFORM)/include/mach	\
	-I$(srctree)/drivers/misc/mediatek/pmic/	\
	-I$(srctree)/drivers/misc/mediatek/pmic/include	\
	-I$(srctree)/drivers/misc/mediatek/pmic/extbuck \
	-I$(srctree)/drivers/misc/mediatek/pmic/include/mt6356	\
	-I$(srctree)/drivers/misc/mediatek/pmic/include/mt6358	\
	-I$(srctree)/drivers/misc/mediatek/thermal/mt6877/inc/mach  \
	-I$(srctree)/drivers/misc/mediatek/base/power/include/gpufreq_v1/  \
	-I$(srctree)/drivers/gpu/mediatek/gpufreq/   \
	-I$(srctree)/drivers/gpu/mediatek/ged/include/   \
	-I$(srctree)/drivers/misc/mediatek/thermal/$(CONFIG_MTK_PLATFORM)/inc/mach	\
	-I$(srctree)/include/linux/	\
	-I$(srctree)/drivers/misc/mediatek/dramc/$(MTK_PLATFORM)	\
	-I$(EEM_ROOT_DIR)/mt6877/inc	\
	-I$(srctree)/drivers/misc/mediatek/base/power/mcdi/include/

ifeq ($(CONFIG_MTK_TINYSYS_MCUPM_SUPPORT), y)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/mcupm/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/mcupm/$(MTK_PLATFORM)/
endif

ifeq ($(PROJECT_DTB_NAMES),mediatek/k6877v1_64_mcl_k419)
subdir-ccflags-y += -DMC50_LOAD
endif

ifeq ($(PROJECT_DTB_NAMES),mediatek/k6877v1_64_77t_mcl_k419)
subdir-ccflags-y += -DMC50_LOAD
endif

ifeq ($(PROJECT_DTB_NAMES),mediatek/k6877v1_64_77tt_mcl_k419)
subdir-ccflags-y += -DMC50_LOAD
endif

ifeq ($(PROJECT_DTB_NAMES),mediatek/k6877v1_64_120hz_vdo_dphy_mcl_k419)
subdir-ccflags-y += -DMC50_LOAD
endif

ifeq ($(PROJECT_DTB_NAMES),mediatek/k6877v1_64_6gb_mcl_k419)
subdir-ccflags-y += -DMC50_LOAD
endif

obj-y += mtk_eem.o
obj-y += mtk_eem_platform.o
obj-y += mtk_eem_internal.o
obj-y += mtk_eem_api.o

ifeq ($(CONFIG_MTK_BASE_POWER), y)
obj-y += mtk_picachu.o
endif

