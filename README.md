# Mail Alert

## What Is This ?
Mail Alert, uses to alert when you received a message with subject that contains text with specific pattern.

## How To Use ?
Run the mailalert script on shell. It's enough for start to listening your mailbox via IMAP protocol.
```shell
$ ./mailalert
```

## Dependencies
Mail Alert requires **mpg123** package. You can install it with the following command:
```shell
sudo apt-get install mpg123
```

## Configuration
Rename the **conf.py-DIST** file as **conf.py** and edit the file for determining your email configuration, checking period and others:
```python
# -*- coding: utf-8 -*-

IMAP_USER = 'your.name@domain.com'

IMAP_PWD = 'ThisIsYourPassword'

IMAP_HOST = 'imap.yourserver.com'

IMAP_PORT = 993

SUBJECT_PATTERN = r'This your subject pattern as regex'

TMP_FILE = '/tmp/mailalert.tmp'

# Sleep time as second.
SLEEP_TIME = 30

EXECUTE_ON_ALARM = 'mpg123 GodFotherHorn.mp3' 
```
