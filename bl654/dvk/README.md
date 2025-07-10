**BL654 DVK Firmware**

Canvas firmware is distributed as a `.hex` file for use with programming tools such as **nRF Connect**, **nrfutil** or **nrfjprog** to program the internal flash of the module via cabled SWD interface using a J-Link or similar programming adapter. For devices already running Canvas firmware, the `.bin` files can be used to perform OTA firmware update via mobile applications or similar device management tools.

Firmware images are organized into versioned subfolders. Within each versioned subfolder, a `zephyr` subdirectory contains the `.hex` and (when supported) `.bin` files for download.
