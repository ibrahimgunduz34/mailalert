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

TMP_FILE = '/tmp/mailalert.tmp'

# Interval time as second for checking new messages.
CHECKING_INTERVAL = 30

# You can use SUBJECT_PATTERN and EXECUTE_ON_ALARM keys for the specific pattern matching or can use RULES key for checking by multiple pattern matching.

# SUBJECT_PATTERN = r'This your subject pattern as regex'
# EXECUTE_ON_ALARM = 'mpg123 GodFotherHorn.mp3' 

# or

# RULES = (
# 		{'pattern': r'MKF WEB SİTE|MKF WEB SITE|mkf web site',
#		 'exec': 'mpg123 GodFotherHorn.mp3'},
#	)

```
