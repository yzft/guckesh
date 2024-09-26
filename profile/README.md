Tutorial Creating a build environment
-------------------------------------

### Sync ###

----------------------------------
```bash
sudo apt update -y && sudo apt upgrade -y && sudo apt install git-core -y && sudo apt install android-tools-adb android-tools-fastboot -y
```
```bash
git clone --depth 1 git@github.com:Iascker/Iascker.git -b master scripts
cd scripts
bash setup/android_build_env.sh
```
```bash
sudo nano /etc/passwd
```
```bash
ssh-keygen -t ed25519 -C "mezaquegit@gmail.com"
```
```bash
cat /home/aos/.ssh/id_ed25519.pub
```
```bash
sudo apt-get install 2to3 -y
sudo apt-get install python2-minimal:i386 -y
sudo apt-get install python2:i386 -y
sudo apt-get install python2-minimal -y
sudo apt-get install python2 -y
sudo apt-get install dh-python -y
sudo apt-get install python-is-python3 -y
sudo apt-get install python2 -y
sudo apt-get install python3 -y
sudo apt-get install python3.9 -y
sudo apt-get install python3.10 -y
sudo apt-get install python3.11 -y
sudo apt-get install python3-pip -y
sudo apt install python3-pylint-common -y
sudo apt install ccache -y
export USE_CCACHE=1
export CCACHE_DIR=/home/aos/.ccache
ccache -M 150G
mkdir ~/.bin
PATH=~/.bin:$PATH
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo
chmod a+x ~/.bin/repo
sudo apt install git-lfs -y
git lfs install -y
```
```bash
curl -Lo .git/hooks/commit-msg https://review.lineageos.org/tools/hooks/commit-msg
chmod u+x .git/hooks/commit-msg
```
```bash
mkdir alpha
cd alpha
repo init -u https://github.com/alphadroid-project/manifest -b alpha-14 --git-lfs -y
repo sync
repo sync
rm -rf hardware/samsung
git clone git@github.com:Guckesh/android_hardware_samsung hardware/samsung
mkdir hardware/samsung/nfc
rm -rf hardware/qcom-caf/common
git clone git@github.com:Guckesh/android_hardware_qcom-caf_common hardware/qcom-caf/common
git clone git@github.com:Guckesh/android_device_samsung_dm1q device/samsung/dm1q
git clone git@github.com:Guckesh/android_vendor_samsung_dm1q vendor/samsung/dm1q
git clone git@github.com:Guckesh/android_device_samsung_sm8550-common device/samsung/sm8550-common
git clone git@github.com:Guckesh/android_vendor_samsung_sm8550-common vendor/samsung/sm8550-common
git clone git@github.com:Guckesh/android_kernel_samsung_sm8550 kernel/samsung/sm8550
git clone git@github.com:Guckesh/android_kernel_samsung_sm8550-devicetrees kernel/samsung/sm8550-devicetrees
git clone git@github.com:Guckesh/android_kernel_samsung_sm8550-modules kernel/samsung/sm8550-modules
. build/envsetup.sh
lunch lineage_dm1q-userdebug
make bacon
```
### Sync ###

----------------------------------

[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217991103595)](https://t.me/KimiNiTodock)
