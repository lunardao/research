## Secure Data Deletion

*This guide is focused on Linux systems*.

**How Data Deletion Works**

When selecting "delete" or "move to Trash", your data isn't deleted from your storage device. The file's directory entry is removed, but the data and metadata isn't actually destroyed. The data is recoverable with forensic software. The data is only deleted and made irretrievable if overwritten with other data. The command to perform this task is *shred*

```bash
shred
```

-In a linux environment using the ```shred``` command overwrites the specified FILE(s) repeatedly, in order to make it harder for even very expensive hardware probing to recover the data.


