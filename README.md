# mmc-utils
This project is a fork of the MMC utils project at http://git.kernel.org/cgit/linux/kernel/git/cjb/mmc-utils.git/.  Modifcations are made to the original project to initially add support for reading SMART data from Delkin micro SD cards.  The addition of SMART to the micro SD cards is a big benefit as you can monitor key parameters such as percentage life remaining etc.

### SMART SD Card Spec.
The spec. for the Delkin SD cards with SMART support can be downloaded from their website at http://delkinoem.com/oem-login/register-form.php.

### Sample Usage:
  ./mmc readsmart /dev/mmcblk0
  Calculated remaining life   100.00%
  Good block rate             286.86% <-- this a bug that needs to be fixed
  Remaining spare block count 78
  Power cycle count           59
  Abnormal power down count   0

### TODO
Currently we only report a subset of the SMART data read from the card.  The project could be modified to return the full data set if desired.
