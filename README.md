# forge

Email dataset for email signature parsing

## Rationale

When working on a machine learning algorithm to solve some problem there are two most important things: the algorithm itself and the dataset to train / test the algorithm on.

Ever since we open-sourced our signature parsing library [talon](https://github.com/mailgun/talon) we were looking for a way to make the dataset publicly available. So that it would be easier for developers to contribute to the core functionality.

Another objective is to spark collaboration on the dataset itself to make it more representational and up to date.

## Emails Source

The core of the dataset is a subset of [Enron](https://www.cs.cmu.edu/~enron/) data, cleansed of private, health and financial information by [EDRM](http://www.edrm.net/resources/data-sets/edrm-enron-email-data-set).

Feel free to add your own emails but be careful to not include any sensetive information. Extend / use the dataset at your own risk.

## Format

Emails with signatures are in ``dataset/P`` folder (``P`` stands for positive). Emails without, are in ``dataset/N`` folder (``N`` stands for negative).

Each email is represented by two files - ``xyz_body`` has email text, ``xyz_sender`` has sender name / address.

Signature lines are annotated with ``#sig#``. For example:

```
Hi John,

Can we have a meeting tomorrow at 11 AM CST?

#sig#--
#sig#Mike Smith
#sig#555-243-0623
```
