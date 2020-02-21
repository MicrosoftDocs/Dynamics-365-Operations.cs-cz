## <a name="product-number-identified-barcode-to-msdyn_productbarcodes"></a>Čárový kód identifikovaný číslem produktu do msdyn_productbarcodes

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
PRODUCTNUMBER | > | msdyn_productnumberid.msdyn_productnumber | 
BARCODE | > | msdyn_name | 
BARCODE | > | msdyn_barcode | 
PRODUCTQUANTITY | > | msdyn_productquantity | 
PRODUCTDESCRIPTION | > | msdyn_productdescription | 
BARCODESETUPID | > | msdyn_barcodesetupid | 
PRODUCTQUANTITYUNITSYMBOL | > | msdyn_unitofmeasureid.msdyn_symbol | 
ISDEFAULTSCANNEDBARCODE | >> | msdyn_isdefaultscannedbarcode | 
ISDEFAULTPRINTEDBARCODE | >> | msdyn_isdefaultprintedbarcode | 
ISDEFAULTDISPLAYEDBARCODE | >> | msdyn_isdefaultdisplayedbarcode | 
