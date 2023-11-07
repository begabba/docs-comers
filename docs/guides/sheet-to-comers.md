# Sheet-to-comers

Sheet-to-comers is a software that creates events in Comers from data found in COMERS OVERVIEW.
It does this by opening a browser and clicking the necessary buttons in Comers for you.
Sheet-to-comers is currently **only available for Windows** (64-bit) computers.

You'll need to be familiar with how to [Create new events](../guides/create-a-new-event/00.%20Introduction.md) in Comers.

## Installation

Unpack [this]() archive on your Windows computer.  
**TODO: Insert Google Drive download link**

## Configuration

After your first run of Comers-to-sheet a file named `config.cfg` will be created.

| name           | description                                                       |
| -------------- | ----------------------------------------------------------------- |
| username       | Username for Comers login                                         |
| password       | Password for Comers login                                         |
| is_summer_camp | Enables the workaround for summer volunteer events                |
| headless       | If set to `False` the browser is visible while creating the event |
| post_url       | Don't mess with this!                                             |

Open `config.cfg` in `Notepad` or any other text editor to change the settings.

## Creating your first event

- Before starting make sure to run `Validate` from `AwesomeBar` in [COMERS OVERVIEW](https://docs.google.com/spreadsheets/d/1a2BTf9VfGQlScm0UR8xB2wzFnm_yhQC8VP4iIygmMeM/edit?ts=5c07f01d#gid=1416145104).
- Doubleclick **sheet-to-comers.exe** to start Comers-to-sheet in a terminal window.
  : First run of Sheet-to-comers will ask you for Comers login credentials and download necessary Chrome/Chromedriver. You can change the user credentials later by editing `config.cfg` in Notepad.
- **Make sure nobody else is using the login credentials in Comers!**
- Select the event by typing the event PRODUCT_CODE
  : Only events with **STATUS** set to **READY** will be available.
- USE_TEST_SITE?
  : Always create the event with USE_TEST_SITE **"Yes"** first.  
  Answering **"Yes"** will use [testadminang.comers.se](https://testadminang.comers.se) instead of [adminang.comers.se](https://adminang.comers.se)
  !!! Note
  testadminang.comers.se is a mirror of our Comers and is useful for testing things without the risk of breaking something.  
   This allows you to find any remaining issue with the event without having to clean up Comers afterwards.  
   **Any error message Comers outputs will be shown in the terminal. Be sure to read it!**

Now the clicking starts. Do not touch the computer while this is running.  
If this process is interrupted at any time you'll have to either:

1. Complete the process manually by following this [guide](https://begabba.github.io/docs-comers/guides/create-a-new-event/00.%20Introduction/)
2. Remove any traces of the created event from Comers and run Comers-to-sheet again.

When the process is finished **❇ Done! ❇** is shown together with some remaining tasks.

![img](images/done.png)

## Creating summer volunteer camps

The maximum length of an Product price in Comers is 28 days. This is shorter than the "ALL SUMMER"-camps used for volunteers.
The workaround is to set `is_summer_camp` to `True` in `config.cfg` for **all** summer volunteer camps.

Enabling `is_summer_camp` has two major differences:

- No Product capacity is created.
  : Instead it's suggested that you manually create `Freesale` capacity for `VOLPOOL` once for the whole summer . Set the capacity starting date to the _start of the first event_ and capacity end date to the _end of the last event_.

- Sheet-to-comers creates _Product price_ that uses **per-day** price instead of **total** price.
  : Any remaining difference is put on Arrangement price. This might lead to some weird looking prices but the total price will be the same.

![img](images/use_summercamp_tweaks.png)

!!! Important
PRICE_VOLPOOL must be greater than **0** for Comers-to-sheet to work.
You can always massage the Arrangement/Product price after the event is created.

## Troubleshooting

### Comers-to-sheet fails to start

Remove all files and folders except _comers-to-sheet.exe_ and run again.
This should reset everything and force Comers-to-sheet to reinstall it's dependencies.
