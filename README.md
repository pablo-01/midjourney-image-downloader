# midjourney-image-downloader - fork

Fork for my personal use / experiments.

Minor bug fixes and some additonal features.
- bug fix: if prompt conatins quotemarks it will throw: removed quotemarks before file is saved
- added flags to: 
    - SAVE_PROMPT = True : save all prompts of dewnloaded files into a csv file 
    - SAVE_JSON = True   : for each file, save associated json data into file
    - RANDOM_WAIT = True : random wait time, between (0.5, 2) seconds


-------
Download your Midjourney gallery.

Copied from https://github.com/timmc/midjourney-history-sync ⭐ and adapted with additional advice from [timmc](https://github.com/timmc) ️

## About
- Default: saves images in date folders with prompt as filename, eg:
```/midjourney-image-downloader/jobs/2022/10/23/057b9a3b-1f2b-4279-9d27-63a102cbed79/prompt.png``` (Can be disabled: ```USE_DATE_FOLDERS```)
- Default: only saves upscaled images (Can be changed: ```UPSCALES_ONLY```/```GRIDS_ONLY```)
- Safe to stop and resume
- Midjourney API caps paging at 50. This script pages to 50 using all known "orderBy" options to try and get a complete sync with the web gallery. If you have less than 5001 images then you should be able to get a full sync using this script. 

## To run
Install:
 ```pip install -e .```

Run:
```python download.py```

