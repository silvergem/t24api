### Overview
This contains a list of my local development subroutines that will extend T24 functionality

***

### Prerequisites
1. T24 TAFC R12
1. Local table created using EB.TABLE.DEFINITION (BDUH001-GEN.TABLE.xxxxxx.zip)

***
### Local API

| Subroutine             | Type            | Attached on     | Description   | Input Parameters | Output Parameters|
|------------------------|-----------------|-----------------|---------------|------------------|------------------|
| VR.ADD.OFS.REQUEST                  | Version Routine | BEFORE.AUTH.RTN | Add Additional OFS Request at Version Level |||
| VR.VALIDATE.FIELDS.USING.REGEX      | Version Routine | INPUT.ROUTINE   | Validate fields using on REGEX Expression   |||
| BATCH.CREATE.WRITE.FILE             | Batch Routine   |                 | This will create/write file per agent. Files will be merge by BATCH.MERGE.WRITE.FILE routine | Y.FILE.DIR = File Directory <br /> Y.FILENAME = File Name     <br /> Y.FILE.EXT = File extension <br /> Y.RECORD   = Record ||
| BATCH.MERGE.WRITE.FILE              | Batch Routine   |                 | This will merge files created by BATCH.CREATE.WRITE.FILE routine. This will be placed on .POST or .SELECT(Using Control list) file of Batch routine | Y.FILE.DIR  = File Directory <br /> Y.FILENAME  = File Name <br /> Y.TIMESTAMP = Option to place timespamp, Set yo 'Y' |Y.ERR       = Error
***
<b>Deployment Guide </b>

1. Download the API Routine needed
1. Deploy and Catalog the routine on your BP Folder (You can rename or add prefix)

P.S 1: Might work on lower releases
