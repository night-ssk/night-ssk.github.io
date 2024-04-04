pinctrl子系统主要工作内容如下：
①、获取设备树中 pin信息。
②、根据获取到的 pin信息来设置pin的复用功能
③、根据获取到的 pin信息来设置pin的电气特性，比如上/下拉、速度、驱动能力等。

MX6UL_PAD_UART1_RTS_B__GPIO1_IO19  0x17059 
前面的为#define MX6UL_PAD_UART1_RTS_B__GPIO1_IO19 0x0090 0x031C 0x0000 0x5 0x0
<mux_reg conf_reg input_reg mux_mode input_val>