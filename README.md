# Custom STM32 Mechanical Keyboard

This repository contains the hardware design files (PCB schematics and mechanical enclosures) for a custom mechanical keyboard. The PCB is designed in **KiCad**, and the case/mechanical components are modeled in **FreeCAD**.

## Features

* **Microcontroller:** STM32F405RGT
* **Connectivity:** USB-C 2.0 with dedicated ESD protection (USBLC6-2SC6)
* **Switch Matrix:** 6x16 layout supporting up to 96 keys
* **Switches:** Cherry MX compatible, utilizing Khail hot-swap sockets
* **Anti-Ghosting:** Per-key diodes for full N-Key Rollover (NKRO)
* **Extras:** Support for a rotary encoder and broken-out SWD/I2C pins for easy debugging and expansion

## Repository Structure

* `/` - Contains the KiCad project, schematics, and PCB layout files.
* `/case/` - Contains the FreeCAD design files for the keyboard case and plate.
* `/pcbway_production/` - Contains the gerber files.

## Prerequisites & Environment Setup

Before opening the KiCad project files, you need to configure your KiCad environment with the appropriate custom libraries and plugins used in this design. 

### KiCad Package Installation

Follow these steps exactly to ensure all footprints and symbols load correctly:

1. **Add the ebastler repository:**
   * Open KiCad and go to the **Plugin and Content Manager**.
   * Click on **Manage Repositories** (usually at the bottom left).
   * Add a new repository with the following URL:
     [https://raw.githubusercontent.com/ebastler/KiCad-repository/main/repository.json](https://raw.githubusercontent.com/ebastler/KiCad-repository/main/repository.json)
2. **Install custom libraries:**
   * Switch the repository dropdown at the top of the Plugin Manager to the newly added `ebastler` repo.
   * Find and install the **`marbastlib`** package.
3. **Switch back to the official repository:**
   * Change the repository dropdown back to the official **KiCad** repository.
4. **Install required keyboard packages:**
   * Search for and install the **`Keyswitch KiCad Library`**.
   * *(Optional)* If you plan on modifying the PCB layout, install the **`Keyboard footprints placer`** plugin to make routing and placing switches easier.

Once these packages are installed, you can safely open the `.kicad_pro` file.

## Contributions

Feel free to fork this repository and submit pull requests if you have improvements for the PCB routing or case design. 

My Ko-fi link if you wanna support my efforts: ![Ko-fi](kofiLogo_small.svg) [Kofi](https://ko-fi.com/mantaflow)

## Thanks

Inspired from: [Modern Hobbyist](https://www.youtube.com/watch?v=u13yRbBiRYM)

## License
This project is licensed under the **GNU General Public License v3.0 (GPL-3.0)**. See the [LICENSE](LICENSE.txt) file for more details.
