# Sheet-to-comers

DONE: förklara PRODUCT_CODE input
DONE: info.logger supplements done + link/status done
DONE: Fix integer conversion, don't assume type
TODO: add "one discount code for all summer" in todo when using summercamp
TODO: magic wand references
TODO: rename is_summer_camp to USE_SUMMERCAMP_TWEAKS
TODO: cleanup folder (remove zip, move browser)
TODO: Simplify error: Could not create product with product code:

TOOD: filter vol event on summercamp tweak

Sheet-to-comers is a software that creates events in Comers from data found in COMERS OVERVIEW.
It does this by opening a browser and clicking the necessary buttons in Comers for you.
Sheet-to-comers is currently **only available for Windows** (64-bit) computers.

You'll need to be familiar with the process of [Create new events](../guides/create-a-new-event/00.%20Introduction.md) in Comers. Sheet-to-comers follows the exact same steps as the guide.  
If this process is interrupted at any time you'll have to either:

1. Complete the process manually by following the [guide](https://begabba.github.io/docs-comers/guides/create-a-new-event/00.%20Introduction/)
2. Remove any traces of the created event from Comers and run Comers-to-sheet again.

## Installation

You'll find the latest version here: [sheet-to-comers.zip](https://drive.google.com/drive/folders/1UXP9iwGZBtSQwa5v9T6ISEFM0oH853NI?usp=sharing)

## Creating your first event

- Before starting make sure to run `Validate` from `AwesomeBar` in [COMERS OVERVIEW](https://docs.google.com/spreadsheets/d/1a2BTf9VfGQlScm0UR8xB2wzFnm_yhQC8VP4iIygmMeM/edit?ts=5c07f01d#gid=1416145104).
- Doubleclick **sheet-to-comers.exe** to start Comers-to-sheet in a terminal window.
  : First run of Sheet-to-comers will ask you for Comers login credentials and download necessary Chrome/Chromedriver. You can change the user credentials later by editing `config.cfg` in Notepad.
- Windows Defender > mer info > Kör ändå
- **Make sure nobody else is currently using the login credentials in Comers!**
- 
- Select the event by typing the event PRODUCT_CODE
  : Only events with **STATUS** set to **READY** will be available.
- USE_TEST_SITE?
  : Always create the event with USE_TEST_SITE **"Yes"** first.  
  Answering **"Yes"** will use [testadminang.comers.se](https://testadminang.comers.se) instead of [adminang.comers.se](https://adminang.comers.se)  
  testadminang.comers.se is a mirror of our Comers and is useful for testing things without the risk of breaking something.  
  This allows you to find any remaining issue with the event without having to clean up Comers afterwards.  
  **Any error message Comers outputs will be shown in the terminal. Be sure to read it!**

Now the clicking starts. Do not touch the computer while this is running.  

When the process is finished **❇ Done! ❇** is shown together with some remaining tasks.

![img](images/done.png)

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

## Creating summer volunteer camps

The maximum length of an Product price in Comers is 28 days. This is shorter than the "ALL SUMMER"-camps used for volunteers.
The workaround is to set `is_summer_camp` to `True` in `config.cfg` before creating any of the summer volunteer camps.

!!! Important
    PRICE_VOLPOOL must be greater than **0** for Comers-to-sheet to work.
    You can always massage the Arrangement/Product price after the event is created.

Enabling `is_summer_camp` has two major differences:

- No Product capacity is created.
  : Instead it's suggested that you manually create `Freesale` capacity for `VOLPOOL` once for the whole summer . Set the capacity starting date to the _start of the first event_ and capacity end date to the _end of the last event_.

- Sheet-to-comers creates _Product price_ that uses **per-day** price instead of **total** price.
  : Any remaining difference is put on Arrangement price. This might lead to some weird looking prices but the total price will be the same.

![img](images/use_summercamp_tweaks.png)


## Troubleshooting

### Comers-to-sheet fails to start

Remove all files and reinstall Comers-to-sheet.
This should reset everything and force Comers-to-sheet to reinstall it's dependencies.

<!-- Next you could try to run Comers-to-sheet from a Windows terminal. -->
<!-- * TODO: Screenshot -->
<!-- * Right-click in Comers-to-sheet folder -->
<!-- * Click open ... -->
<!-- * Write `comers-to-sheet.exe` and press enter -->
<!-- : This will prevent the window from automatically closing and give the opportunity to read any error message. -->
