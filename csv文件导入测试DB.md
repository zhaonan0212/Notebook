## csv文件导入测试DB

#### 1.TBLEMSEQPACCSTATE

```
create table TBLEMSEQPACCSTATE(
		EQUIPMENTTYPE VARCHAR2(50),
		EQUIPMENTNO VARCHAR2(50),
		ACCESSORYTYPE VARCHAR2(50),
		ACCESSORYNO VARCHAR2(50),
		USERNO VARCHAR2(10),
		STARTTIME DATE,
		ACCESSORYVERSION VARCHAR2(3)	
)
```

#### 2.TBLEMSEQPACCSTATELOG

```
create table TBLEMSEQPACCSTATELOG(
		ACCSERIALNO  VARCHAR2(20),
		EQUIPMENTTYPE VARCHAR2(50),
		EQUIPMENTNO VARCHAR2(50),
		ACCESSORYTYPE VARCHAR2(50),
		ACCESSORYNO VARCHAR2(50),
		ACCESSORYVERSION VARCHAR2(3),
		USERNO VARCHAR2(10),
		STARTTIME DATE,
		ENDTIME DATE
)
```

#### 3.TBLEMSEQPMFUHISTORY

```
create table TBLEMSEQPMFUHISTORY(
		EQUIPMENTNO VARCHAR2(50),
		SIDEID VARCHAR2(25),
		MFUNO VARCHAR2(10),
		MFUACTION NUMBER(2,0),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE
)
```

#### 4.TBLEMSEQPMFUSTATUS

```
create table TBLEMSEQPMFUSTATUS(
		EQUIPMENTNO VARCHAR2(50),
		SIDEID VARCHAR2(25),
		MFUNO VARCHAR2(10),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		COMPUTERNAME VARCHAR2(30)
)
```

#### 5.TBLEQPACCCATEGORYSTATEBASIS

```
create table TBLEQPACCCATEGORYSTATEBASIS(
		ACCESSORYCATEGORY VARCHAR2(50),
		ACCESSORYSTATE NUMBER(2,0),
		ACCESSORYSTATENAME VARCHAR2(50),
		INITIALFLAG NUMBER(1,0),
		ISSUESTATE NUMBER(1,0),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		OPERATIONNAME VARCHAR2(50),
		INTERFACENAME VARCHAR2(50)
)
```

#### 6.TBLEQPACCESSORYBASIS

```
create table TBLEQPACCESSORYBASIS(
		ACCESSORYNO VARCHAR2(50),
		ACCESSORYTYPE VARCHAR2(50),
		VENDORNO VARCHAR2(50),
		MODELNO VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0),
		ASSETNO VARCHAR2(50),
		ACCESSORYVERSION VARCHAR2(3),
		CURVERSION NUMBER(1,0),
		ACCESSORYCATEGORY VARCHAR2(50),
		STOCKERNO VARCHAR2(50),
		APSERIALNO VARCHAR2(20),
		MONO VARCHAR2(20)
)
```

#### 7.TBLEQPACCESSORYCATEGORY

```
create table TBLEQPACCESSORYCATEGORY(
		ACCESSORYCATEGORY VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)
)
```

#### 8.TBLEQPACCESSORYCLEAN

```
create table TBLEQPACCESSORYCLEAN(
		ACCESSORYNO VARCHAR2(50),
		STOCKERNO VARCHAR2(50),
		STATUS NUMBER(2,0),
		TENSION1 VARCHAR2(10),
		TENSION2 VARCHAR2(10),
		TENSION3 VARCHAR2(10),
		TENSION4 VARCHAR2(10),
		TENSION5 VARCHAR2(10),
		SURFACE VARCHAR2(10),
		CLEANDATE DATE,
		TENSIONDATE DATE,
		ACCSERIALNO VARCHAR2(50),
		CREATEDATE DATE,
		MONO VARCHAR2(50)
)
```

#### 9.TBLEQPACCESSORYLIFE

```
create table TBLEQPACCESSORYLIFE(
		ACCESSORY VARCHAR2(50),
		LIFEMANAGE NUMBER(2,0),
		LIFESCRIPT VARCHAR2(200),
		REPAIRABLE NUMBER(2,0),
		REPAIRCYCLE NUMBER(8,0),
		SCRAPTYPE NUMBER(2,0),
		SCRAPLIFE NUMBER(8,0),
		LIFETOLERANCE NUMBER(2,0),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		REVISER VARCHAR2(10),
		REVISEDATE DATE
)
```

#### 10.TBLEQPACCESSORYMAINTAIN_DELTA

```
create table TBLEQPACCESSORYMAINTAIN_DELTA(
		ACCESSORYTYPE VARCHAR2(50),
		ACCESSORYNO VARCHAR2(50),
		MAINTAINNO VARCHAR2(50),
		MAINTAINCYCLE NUMBER(5,0),
		MAINTAINNUMBER NUMBER(5,0),
		ALERTCYCLE NUMBER(5,0),
		ALERTNUMBER NUMBER(5,0),
		DESCRIPTION VARCHAR2(4000),
		ISSUESTATE NUMBER(1,0),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE
)
```

#### 11.TBLEQPACCESSORYPROPERTY

```
create table TBLEQPACCESSORYPROPERTY(
		ACCESSORY VARCHAR2(50),
		PROPERTYNO VARCHAR2(20),
		DEFAULTVALUE VARCHAR2(255),
		PROPERTYSEQUENCE NUMBER(2,0),
		DESCRIPTION VARCHAR2(255),
		ISSUESTATE NUMBER(1,0),
		ACCESSORYVERSION VARCHAR2(3)
)
```

#### 12.TBLEQPACCESSORYTYPE

```
create table TBLEQPACCESSORYTYPE(
		ACCESSORYTYPE VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0),
		ACCESSORYCATEGORY VARCHAR2(50),
		RETURNCHECKTYPE NUMBER(2,0)
)
```

#### 13.TBLEQPACCSTATEBASIS

```
create table TBLEQPACCSTATEBASIS(
		ACCESSORYSTATE NUMBER(2,0),
		STATETYPE NUMBER(2,0),
		STATENAME VARCHAR2(50),
		STATECOLOR NUMBER(11,0),
		DESCRIPTION VARCHAR2(255)
)
```

#### 14.TBLEQPACCSTATECONTROL

```
create table TBLEQPACCSTATECONTROL(
		CONTROLTYPE VARCHAR2(50),
		CONTROLNO VARCHAR2(50),
		ACCESSORYSTATE NUMBER(2,0)
)
```

#### 15.TBLEQPCARRIERBASIS

```
create table TBLEQPCARRIERBASIS(
		CARRIERNO VARCHAR2(50),
		CARRIERCATEGORY VARCHAR2(50),
		CARRIERTYPE VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)
)
```

#### 16.TBLEQPCARRIERCATEGORY

```
create table TBLEQPCARRIERCATEGORY(
		CARRIERCATEGORY VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)	
)
```

#### 17.TBLEQPCARRIERSTATE_DELTA

```
create table TBLEQPCARRIERSTATE_DELTA(
		CARRIERNO VARCHAR2(50),
		CARRIERCLASS NUMBER(2,0),
		NORMALQTY NUMBER(4,0),
		RESERVEQTY NUMBER(4,0),
		MOCOMBINENO VARCHAR2(50)
)
```

#### 18.TBLEQPCARRIERTYPE

```
create table TBLEQPCARRIERTYPE(
		CARRIERTYPE VARCHAR2(50),
		CARRIERCATEGORY VARCHAR2(50),
		USELAYER NUMBER(1,0),
		CARRIERLAYER NUMBER(3,0),
		CARRIERCAPACITY NUMBER(3,0),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0),
		STARTPOSITION NUMBER(1,0)
)
```

#### 19.TBLEQPEQUIPMENTTYPE_PICTURE   

```
create table TBLEQPEQUIPMENTTYPE_PICTURE(
		PICTURENAME varchar2(50),
		PICTUREBODY BLOB
)
```

#### 20.TBLEQPFEEDERTYPE

```
create table TBLEQPFEEDERTYPE(
		FEEDERTYPE VARCHAR2(25),
		CYCLETIME NUMBER(3,0),
		QUANTITY NUMBER(8,0),
		ALARMCYCLETIME NUMBER(3,0),
		ALARMQUANTITY NUMBER(8,0),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE		
)
```

#### 21.TBLEQPGROUPBASIS

```
create table TBLEQPGROUPBASIS(
		EQUIPMENTGROUP VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)
)
```

#### 22.TBLEQPGROUPDETAIL

```
create table TBLEQPGROUPDETAIL(
		EQUIPMENTGROUP VARCHAR2(50),
		EQUIPMENTNO VARCHAR2(50)	
)
```

#### 23.TBLEQPLOSSLOG

```
create table TBLEQPLOSSLOG(
		UNLOCKEDID VARCHAR2(50),
		COMBINEPICKUPNO VARCHAR2(50),
		MATERIALNO VARCHAR2(50),
		EQPLOSSQTY NUMBER(20,0),
		PRODUCTNO VARCHAR2(50),
		WEEKLY VARCHAR2(50),
		ENGTYPE VARCHAR2(30),
		UPDATETIME DATE,
		UPDATEBY VARCHAR2(50),
		SLOT VARCHAR2(25),
		SIDEID VARCHAR2(25),
		EQUIPMENTSEQ VARCHAR2(25),
		UNLOCKDESCRIPTION VARCHAR2(200),
		USEDQTY NUMBER(8,0)
)
```

#### 24.TBLEQPLOSSUNLOCKEDLOG

```
create table TBLEQPLOSSUNLOCKEDLOG(
		UNLOCKEDID  VARCHAR2(50),
		UNLOCKEDTIME DATE,
		UNLOCKEDBY VARCHAR2(50)
)
```

#### 25.TBLEQPQCLISTBASIS 

```
create table TBLEQPQCLISTBASIS(
		QCLISTNO VARCHAR2(100),
         QCLISTNAME VARCHAR2(100),
         QCTYPE NUMBER(2,0),
         UNVALIDACTION NUMBER(2,0),
         DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE
)
```

#### 26.TBLEQPQCLISTDETAIL

```
create table TBLEQPQCLISTDETAIL(
		QCLISTNO VARCHAR2(100),
		QCORDER NUMBER(2,0),
		QCITEM VARCHAR2(1000),
		QCTYPE NUMBER(1,0),
		STDVALUE VARCHAR2(12),
		MAXIVALUE VARCHAR2(12),
		MINIVALUE VARCHAR2(12),
		INPUTDATACOUNT NUMBER(2,0)
)
```

#### 27.TBLEQPRECIPEBASIS

```
create table TBLEQPRECIPEBASIS(
		RECIPEGROUP VARCHAR2(50),
		RECIPEVERSION NUMBER(2,0),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0),
		CURVERSION NUMBER(1,0)
)
```

#### 28.TBLEQPRECIPEDETAIL

```
create table TBLEQPRECIPEDETAIL(
		RECIPEGROUP VARCHAR2(50),
		RECIPEVERSION NUMBER(2,0),
		RECIPENO VARCHAR2(20),
		RECIPEVALUE VARCHAR2(255),
		SEQUENCE NUMBER(2,0),
		DESCRIPTION VARCHAR2(255),
		TYPE NUMBER(1,0),
		STDVALUE NUMBER(8,4),
		MAXIMUM NUMBER(8,4),
		MINIMUM NUMBER(8,4)	
)
```

#### 29.TBLEQPSTATEBASIS

```
create table TBLEQPSTATEBASIS(
		EQUIPMENTSTATE NUMBER(2,0),
		STATETYPE NUMBER(2,0),
		STATENAME VARCHAR2(50),
		STATECOLOR NUMBER(11,0),
		DESCRIPTION VARCHAR2(255),
		ENGINEERGROUPNO VARCHAR2(20)	
)
```

#### 30.TBLEQPSTATECONTROL

```
create table TBLEQPSTATECONTROL(
		CONTROLTYPE VARCHAR2(50),
		CONTROLNO VARCHAR2(50),
		EQUIPMENTSTATE NUMBER(2,0),
		STATENAME VARCHAR2(50)
)
```

#### 31.TBLEQPTOOLBASIS

```
create table TBLEQPTOOLBASIS(
		TOOLNO VARCHAR2(20),
		TOOLNAME VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)
)
```

#### 32.TBLEQPVENDOR

```
create table TBLEQPVENDOR(
		VENDORNO VARCHAR2(20),
		VENDORNAME VARCHAR2(50),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)
)
```

#### 33.TBLEQPVENDORCONTACTOR

```
create table TBLEQPVENDORCONTACTOR(
		VENDORNO VARCHAR2(20),
		CONTACTORNAME VARCHAR2(50),
		TELNO VARCHAR2(20),
		FAXNO VARCHAR2(20),
		TITLE VARCHAR2(20),
		ADDRESS VARCHAR2(50),
		EMAIL VARCHAR2(50),
		DESCRIPTION VARCHAR2(255)
)
```

#### 34.TBLPRSNODEBASIS

```
create table  TBLPRSNODEBASIS(
	     NODEID varchar2(100),
      	 NODENO varchar2(100),
      	 NODETYPE number(1,0),
      	 PROCESSNO varchar2(100),
     	 GROUPNO varchar2(30),
     	 CREATOR varchar2(10),
      	 CREATEDATE date,
   	     DESCRIPTION varchar2(50),
 	     PROCESSVERSION varchar2(3),
         NODEVERSION varchar2(3),
         STAGENO varchar2(50),
         SEQUENCE number(4,0),
         ENGNO varchar2(30)
)
```

#### 35.TBLPRSNODERELATION

```
create table TBLPRSNODERELATION(
	     FROMNODEID varchar2(100),
	     TONODEID varchar2(100),
	     LINKNAME varchar2(30),
	     FROMNODENO varchar2(100),
	     TONODENO varchar2(100),
	     PROCESSNO varchar2(100),
	     PROCESSVERSION varchar2(3)
)
```

#### 36.TBLPRSNODEXML_CLOB

```
create table TBLPRSNODEXML_CLOB(
		PROCESSNO VARCHAR2(100),
		PROCESSVERSION VARCHAR2(3),
		NODEXMLSTRING CLOB		
)
```

#### 37.TBLPRSPROCESSBASIS

```
create table TBLPRSPROCESSBASIS(
		PROCESSNO VARCHAR2(100),
		PROCESSCLASS NUMBER(2,0),
		PSNO VARCHAR2(50),
		PROCESSTYPE VARCHAR2(20),
		ISSUESTATE NUMBER(1,0),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		DESCRIPTION VARCHAR2(255),
		NODEXMLSTRING LONG(0),
		TUNINGPROCESS  NUMBER(1,0),
		PROCESSVERSION VARCHAR2(3),
		CURVERSION NUMBER(1,0)
)
```

#### 38.TBLPRSPROCESSPROPERTY

```
create table TBLPRSPROCESSPROPERTY(
		PROCESSNO VARCHAR2(100),
		PROPERTYNO VARCHAR2(20),
		DEFAULTVALUE VARCHAR2(255),
		PROPERTYSEQUENCE NUMBER(2,0),
		DESCRIPTION VARCHAR2(255),
		ISSUESTATE NUMBER(1,0),
		PROCESSVERSION VARCHAR2(3)
)
```

#### 39.TBLPRSPRODUCTIONSEGMENT

```
create table TBLPRSPRODUCTIONSEGMENT(
		PSNO VARCHAR2(50),
		PSNAME VARCHAR2(50),
		PSORDER NUMBER(2,0),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		DESCRIPTION VARCHAR2(255),
		ISSUESTATE NUMBER(1,0),
		HAVECOMPONENT NUMBER(1,0),
		HAVELEVEL NUMBER(1,0)
)
```

#### 40.TBLPRSTYPE

```
create table TBLPRSTYPE(
		PROCESSTYPE VARCHAR2(20),
		DESCRIPTION VARCHAR2(255),
		CREATOR VARCHAR2(10),
		CREATEDATE DATE,
		ISSUESTATE NUMBER(1,0)
)
```

