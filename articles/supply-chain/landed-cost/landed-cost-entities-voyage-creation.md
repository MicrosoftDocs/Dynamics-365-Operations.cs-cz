---
title: Entity vytváření plavby
description: Tento článek poskytuje informace o datových entitách vytváření cesty, které seskupují datové entity nutné k vytvoření pracovní cesty.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cb2e2f53942015caf9462692515f24deb9689aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873891"
---
# <a name="voyage-creation-entities"></a>Entity vytváření cesty

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Datové entity vytváření cesty seskupují datové entity nutné k vytvoření pracovní cesty. Vy nebo váš speditér můžete tyto datové entity použít k vytvoření záznamů o cestě, přepravním kontejneru, foliu a záznamů řádků cesty, které odkazují na existující řádky nákupní objednávky nebo převodního příkazu.

## <a name="voyages-itmtableentity"></a>Cesty (ITMTableEntity)

Cesta představuje cestu příchozího zboží a slouží jako nákladová oblast nejvyšší úrovně v nákladech za doručení. Obsahuje informace na úrovni záhlaví, které se týkají plavidla a výchozího a cílového přístavu. Tato funkce je podporována entitou `ITMTableEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Způsob dodání | ITMTable.DlvModeId | Nvarchar(10) | Číslo | Číslo |
| Doporučeno zprostředkovatelem | ITMTable.ITMBrokerAdvised | Datum a čas | Číslo | Číslo |
| Schůzka zákazníka | ITMTable.ITMCustomerAppointment | Datum a čas | Číslo | Číslo |
| Doručeno na sklad | ITMTable.ITMDelAtWarehouse | Datum a čas | Číslo | Číslo |
| Instrukce k doručení | ITMTable.ITMDeliveryInstructions | Datum a čas | Číslo | Číslo |
| Datum odjezdu | ITMTable.ITMDepartureDate | Datum a čas | Číslo | Číslo |
| Uvolněné zboží | ITMTable.ITMGoodsReleased | Datum a čas | Číslo | Číslo |
| Datum místní přepravy | ITMTable.ITMLocalTransportDate | Datum a čas | Číslo | Číslo |
| Čas místní přepravy | ITMTable.ITMLocalTransportTime | Int | Číslo | Číslo |
| Byl odeslán původní přepravní doklad | ITMTable.ITMOriginalBOLSebt | Datum a čas | Číslo | Číslo |
| Přijaté původní dokumenty | ITMTable.ITMOriginalDocsReceived | Datum a čas | Číslo | Číslo |
| Stav nákupní objednávky | ITMTable.ITMPurchStatus | Int | Číslo | Číslo |
| Datum ověření | ITMTable.ITMVerificationDate | Datum a čas | Číslo | Číslo |
| Identifikátor celního záznamu | ITMTable.ShipCustomsEntryId | Nvarchar(20) | Číslo | Číslo |
| Datum expedice | ITMTable.ShipDate | Datum a čas | Číslo | Číslo |
| Popis | ITMTable.ShipDescription | Nvarchar(60) | Číslo | Číslo |
| Přijaté dokumenty | ITMTable.ShipDocReceived | Int | Číslo | Číslo |
| Odhadované datum doručení | ITMTable.ShipEstDlvDate | Datum a čas | Číslo | Číslo |
| Odhadovaný čas doručení do přístavu | ITMTable.ShipEstPortDate | Datum a čas | Číslo | Číslo |
| Výchozí přístav | ITMTable.ShipFromPort | Nvarchar(20) | Číslo | Číslo |
| Letecký nákladní list / přepravní doklad | ITMTable.ShipHAWB | Nvarchar(20) | Číslo | Číslo |
| Cesta | ITMTable.ShipId | Nvarchar(20) | **Ano** | **Ano** |
| Odkaz na rezervaci | ITMTable.ShipIdExternal | Nvarchar(20) | Číslo | Číslo |
| Šablona cesty | ITMTable.ShipJourneyId | Nvarchar(20) | Číslo | Číslo |
| Místní dopravce | ITMTable.ShipLocalForwarder | Nvarchar(20) | Číslo | Číslo |
| Hlavní letecký nákladní list / přepravní doklad | ITMTable.ShipMAWB | Nvarchar(20) | Číslo | Číslo |
| Měrný systém | ITMTable.ShipMeasurement | Numeric(32, 6) | Číslo | Číslo |
| Měrná jednotka | ITMTable.ShipMeasurementUnit | Int | Číslo | Číslo |
| Počet palet | ITMTable.ShipNoOfPallets | Int | Číslo | Číslo |
| Čekající cesta | ITMTable.ShipPending | Int | Číslo | Číslo |
| Poznámky | ITMTable.ShipRemarks | Nvarchar(MAX) | Číslo | Číslo |
| Vypůjčení | ITMTable.ShipRental | Int | Číslo | Číslo |
| Stav cesty | ITMTable.ShipStatusId | Nvarchar(20) | Číslo | Číslo |
| Nesouhlas v čísle | ITMTable.ShipTallyInNumber | Nvarchar(20) | Číslo | Číslo |
| Cílový přístav | ITMTable.ShipToPort | Nvarchar(20) | Číslo | Číslo |
| Datum ocenění | ITMTable.ShipValuationDate | Datum a čas | Číslo | Číslo |
| Dopravní společnost | ITMTable.ShipVendAccount | Nvarchar(20) | Číslo | Číslo |
| Plavidlo | ITMTable.ShipVesselId | Nvarchar(20) | Číslo | **Ano** |
| Externí ID cesty | ITMTable.ShipVoyage | Nvarchar(20) | Číslo | Číslo |

### <a name="number-sequences-for-voyages"></a>Číselné řady pro cesty

Sdílená číselná řada pro cesty řídí přidělení ID cesty.

Hodnota, která je předána datové entitě jako **ID cesty** (`ShipId`) se používá k identifikaci existujícího záznamu pro aktualizaci. Pokud tento záznam neexistuje, chování závisí na tom, zda je přiřazená číselná řada konfigurována tak, aby umožňovala ruční zadání:

- Pokud je povoleno ruční zadávání, vytvoří se nový záznam, který používá předanou hodnotu.
- Pokud ruční zadávání není povoleno, použije se místo předané hodnoty další číslo v přiřazené číselné řadě.

Během relace importu se zachová zástupná hodnota, která je importována jako ID cesty. Toto chování zajišťuje, že řádky přepravního kontejneru a cesty, které odkazují na zástupný symbol, budou zahrnuty do cesty a že budou aktualizovány tak, aby odrážely hodnotu přiřazenou z číselné řady.

### <a name="automatic-cost-transactions"></a>Automatické nákladové transakce

K cestě lze připočítat automatické náklady ze stránky **Automatické náklady** v aplikaci Microsoft Dynamics 365 Supply Chain Management (**Náklady za doručení \> Nastavení výpočtu nákladů \> Automatické náklady**). Záznamy pro automatické náklady lze také vytvořit pomocí datových entit nákladových transakcí pro každou nákladovou oblast, kterou modul Náklady za doručení podporuje.

Automatické náklady, které jsou konfigurovány v Supply Chain Management, jsou aplikovány na cestu, když je vytvořen řádek cesty. U záznamu nebudou viditelné žádné náklady, dokud nebude záznam záhlaví spojen s informacemi řádku.

## <a name="shipping-containers-itmcontainersentity"></a>Přepravní kontejnery (ITMContainersEntity)

Přepravní kontejner představuje fyzický kontejner, ve kterém je zboží přepravováno. Tento fyzický kontejner může být nákladním kontejnerem pro námořní přepravu nebo jednou paletou pro leteckou přepravu. Přepravní kontejner obsahuje informace na úrovni záhlaví, které souvisí s ID přepravního kontejneru, číslem plomby a typem přepravního kontejneru. (Typ přepravního kontejneru poskytuje informace o rozměrech.) Tuto funkci podporuje entita `ITMContainersEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Datum odjezdu | ITMContainers.ITMDepartureDate | Datum a čas | Číslo | Číslo |
| Datum místní přepravy | ITMContainers.ITMLocalTransportDate | Datum a čas | Číslo | Číslo |
| Čas místní přepravy | ITMContainers.ITMLocalTransportTime | Int | Číslo | Číslo |
| Původní cesta | ITMContainers.OrigShipId | Nvarchar(20) | Číslo | Číslo |
| Skutečná hmotnost | ITMContainers.ShipActualWeight | Numeric(32, 6) | Číslo | Číslo |
| Doporučeno zprostředkovatelem | ITMContainers.ShipBrokerAdvised | Datum a čas | Číslo | Číslo |
| Přepravní kontejner | ITMContainers.ShipContainerId | Nvarchar(20) | **Ano** | **Ano** |
| Typ přepravního kontejneru | ITMContainers.ShipContainerTypeId | Nvarchar(20) | Číslo | Číslo |
| Typ jednotky | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | Číslo | Číslo |
| Převedeno na pronájem | ITMContainers.ShipConvertedToRental | Int | Číslo | Číslo |
| Schůzka zákazníka | ITMContainers.ShipCustomerAppointment | Datum a čas | Číslo | Číslo |
| Datum expedice | ITMContainers.ShipDate | Datum a čas | Číslo | Číslo |
| Doručeno na sklad | ITMContainers.ShipDelAtWarehouse | Datum a čas | Číslo | Číslo |
| Instrukce k doručení | ITMContainers.ShipDeliveryInstructions | Datum a čas | Číslo | Číslo |
| Datum uplatnění osvědčení o zkoušce | ITMContainers.ShipECAppliedDate | Datum a čas | Číslo | Číslo |
| Datum vypršení osvědčení o zkoušce | ITMContainers.ShipECExpiryDate | Datum a čas | Číslo | Číslo |
| Číslo osvědčení o zkoušce | ITMContainers.ShipECNum | Nvarchar(20) | Číslo | Číslo |
| Datum přijetí osvědčení o zkoušce | ITMContainers.ShipECReceivedDate | Datum a čas | Číslo | Číslo |
| Odhadované datum doručení | ITMContainers.ShipEstDlvDate | Datum a čas | Číslo | Číslo |
| Odhadovaný čas doručení do přístavu | ITMContainers.ShipEstPortDate | Datum a čas | Číslo | Číslo |
| Očekávané datum naložení | ITMContainers.ShipExpectedLoadingDate | Datum a čas | Číslo | Číslo |
| Výchozí přístav | ITMContainers.ShipFromPort | Nvarchar(20) | Číslo | Číslo |
| Popis zboží | ITMContainers.ShipGoodsDesc | Nvarchar(60) | Číslo | Číslo |
| Uvolněné zboží | ITMContainers.ShipGoodsReleased | Datum a čas | Číslo | Číslo |
| Sledovací jednotka GPS | ITMContainers.ShipGPSUnit | Nvarchar(30) | Číslo | Číslo |
| Letecký nákladní list / přepravní doklad | ITMContainers.ShipHAWB | Nvarchar(20) | Číslo | Číslo |
| Cesta | ITMContainers.ShipId | Nvarchar(20) | **Ano** | **Ano** |
| Šablona cesty | ITMContainers.ShipJourneyId | Nvarchar(20) | Číslo | Číslo |
| Místní dopravce | ITMContainers.ShipLocalForwarder | Nvarchar(20) | Číslo | Číslo |
| Měrný systém | ITMContainers.ShipMeasurement | Numeric(32, 6) | Číslo | Číslo |
| Měrná jednotka | ITMContainers.ShipMeasurementUnit | Int | Číslo | Číslo |
| Počet kartonů | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | Číslo | Číslo |
| Byl odeslán původní přepravní doklad | ITMContainers.ShipOriginalBOLSebt | Datum a čas | Číslo | Číslo |
| Přijaté původní dokumenty | ITMContainers.ShipOriginalDocsReceived | Datum a čas | Číslo | Číslo |
| Naše číslo plomby | ITMContainers.ShipOurSealNum | Nvarchar(20) | Číslo | Číslo |
| Použito | ITMContainers.ShipPendingUsed | Int | Číslo | Číslo |
| Stav nákupní objednávky | ITMContainers.ShipPurchStatus | Int | Číslo | Číslo |
| Typ chlazení | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | Číslo | Číslo |
| Poznámky | ITMContainers.ShipRemarks | Nvarchar(MAX) | Číslo | Číslo |
| Vypůjčení | ITMContainers.ShipRental | Int | Číslo | Číslo |
| Vratný | ITMContainers.ShipReturnable | Int | Číslo | Číslo |
| Stav cesty | ITMContainers.ShipStatusId | Nvarchar(20) | Číslo | Číslo |
| Číslo plomby dopravní společnosti | ITMContainers.ShipTheirSealNum | Nvarchar(20) | Číslo | Číslo |
| Cílový přístav | ITMContainers.ShipToPort | Nvarchar(20) | Číslo | Číslo |
| Datum ověření | ITMContainers.ShipVerificationDate | Datum a čas | Číslo | Číslo |
| Plavidlo | ITMContainers.ShipVesselId | Nvarchar(20) | Číslo | **Ano** |

### <a name="voyage-id-validation"></a>Ověření ID cesty

ID přepravního kontejneru není řízeno číselnou řadou. Je unikátní pouze v kontextu cesty, na které se používá.

Pokud se entita přepravního kontejneru (`ITMContainersEntity`) používá nezávisle na entitě cesty (`ITMTableEntity`), hodnota **ID cesty** (`ShipId`) musí odpovídat existujícímu záznamu v tabulce cesty. V opačném případě se import nezdaří.

Pokud se entita přepravního kontejneru (`ITMContainersEntity`) a entita cesty (`ITMTableEntity`) používají jako součást stejné relace importu, musí entita cesty předcházet vytvoření přepravního kontejneru. V opačném případě nelze hodnotu **ID cesty** (`ShipId`) úspěšně ověřit. Pokud je pro **ID cesty** (`ShipId`) použita zástupná hodnota, lze asociaci vytvořit pouze v případě, že je použit stejný zástupný symbol jako **ID cesty** (`ShipId`) v entitě přepravního kontejneru.

### <a name="other-field-validations"></a>Ověřování jiných polí

Následující tabulka ukazuje pole v tabulce přepravních kontejnerů (`ITMContainers`), které jsou ověřeny podle tabulek nastavení nákladů za doručení. Zobrazuje také datové entity nákladů za doručení, které může speditér použít k načtení existujících hodnot a zajištění přijetí platných hodnot ve vašem prostředí.

| Pole v tabulce ITMContainers | Entita dat nákladů za doručení |
|---|---|
| Typ přepravního kontejneru | ITMShippingContainerTypeEntity |
| Popis zboží | ITMGoodsDescriptionEntity |
| Typ chlazení | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>Folia (ITMFolioEntity)

Folio představuje seskupení položek v přepravním kontejneru pro účely celních prohlášení. Folio obsahuje informace na úrovni záhlaví, které se týkají celního zprostředkovatele, a popis zboží. Tato funkce je podporována entitou `ITMFolioEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Doporučeno zprostředkovatelem | ITMFolioTable.ShipBrokerAdvised | Datum a čas | Číslo | Číslo |
| Kontrolní číslo nákladu | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | Číslo | Číslo |
| Schůzka zákazníka | ITMFolioTable.ShipCustomerAppointment | Datum a čas | Číslo | Číslo |
| Celní deklarant | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | Číslo | Číslo |
| ID cla | ITMFolioTable.ShipCustomsId | Nvarchar(60) | Číslo | Číslo |
| Společnost | ITMFolioTable.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Doručeno na sklad | ITMFolioTable.ShipDelAtWarehouse | Datum a čas | Číslo | Číslo |
| Instrukce k doručení | ITMFolioTable.ShipDeliveryInstructions | Datum a čas | Číslo | Číslo |
| Přijaté dokumenty | ITMFolioTable.ShipDocReceived | Int | Číslo | Číslo |
| Odhadované datum doručení | ITMFolioTable.ShipEstDlvDate | Datum a čas | Číslo | Číslo |
| Odhadovaný čas doručení do přístavu | ITMFolioTable.ShipEstPortDate | Datum a čas | Číslo | Číslo |
| Vývozce | ITMFolioTable.ShipExporterId | Nvarchar(20) | Číslo | Číslo |
| Jméno | ITMFolioTable.ShipExporterName | Nvarchar(60) | Číslo | Číslo |
| Datum folia | ITMFolioTable.ShipFolioDate | Datum a čas | Číslo | Číslo |
| Folio | ITMFolioTable.ShipFolioId | Nvarchar(20) | **Ano** | **Ano** |
| Výchozí přístav | ITMFolioTable.ShipFromPort | Nvarchar(20) | Číslo | Číslo |
| Popis zboží | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | Číslo | Číslo |
| Uvolněné zboží | ITMFolioTable.ShipGoodsReleased | Datum a čas | Číslo | Číslo |
| Letecký nákladní list / přepravní doklad | ITMFolioTable.ShipHAWB | Nvarchar(20) | Číslo | Číslo |
| Cesta | ITMFolioTable.ShipId | Nvarchar(20) | Číslo | **Ano** |
| Měrný systém | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | Číslo | Číslo |
| Měrná jednotka | ITMFolioTable.ShipMeasurementUnit | Int | Číslo | Číslo |
| Počet kartonů | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | Číslo | Číslo |
| Byl odeslán původní přepravní doklad | ITMFolioTable.ShipOriginalBOLSebt | Datum a čas | Číslo | Číslo |
| Přijaté původní dokumenty | ITMFolioTable.ShipOriginalDocsReceived | Datum a čas | Číslo | Číslo |
| Stav nákupní objednávky | ITMFolioTable.ShipPurchStatus | Int | Číslo | Číslo |
| Poznámky | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | Číslo | Číslo |
| Stav cesty | ITMFolioTable.ShipStatusId | Nvarchar(20) | Číslo | Číslo |
| Tarifní kód | ITMFolioTable.ShipTariffCode | Nvarchar(10) | Číslo | Číslo |
| Cílový přístav | ITMFolioTable.ShipToPort | Nvarchar(20) | Číslo | Číslo |
| Datum ocenění | ITMFolioTable.ShipValuationDate | Datum a čas | Číslo | Číslo |
| Datum ověření | ITMFolioTable.ShipVerificationDate | Datum a čas | Číslo | Číslo |
| Účet dodavatele | ITMFolioTable.VendAccount | Nvarchar(20) | Číslo | Číslo |

### <a name="number-sequences-for-folios"></a>Číselné řady pro folia

Číselná řada pro folia řídí přidělení ID folia.

Hodnota, která je předána datové entitě jako **ID folia** (`FolioId`) se používá k identifikaci existujícího záznamu pro aktualizaci. Pokud tento záznam neexistuje, chování závisí na tom, zda je přiřazená číselná řada konfigurována tak, aby umožňovala ruční zadání:

- Pokud je povoleno ruční zadávání, vytvoří se nový záznam, který používá předanou hodnotu.
- Pokud ruční zadávání není povoleno, použije se místo předané hodnoty další číslo v přiřazené číselné řadě.

Během relace importu se zachová zástupná hodnota, která je importována jako ID folia. Toto chování zajišťuje, že řádky přepravního kontejneru a cesty, které odkazují na zástupný symbol, jsou správně asociovány a budou aktualizovány tak, aby odrážely hodnotu přiřazenou z číselné řady.

### <a name="field-validations"></a>Ověření polí

Pole **Popis zboží** v tabulce folia (`ITMFolioTable`) je ověřeno podle stejnojmenné tabulky nastavení nákladů za doručení. Speditér může použít datovou entitu nákladů za doručení `ITMGoodsDescriptionEntity` k načtení existujících hodnot a zajištění přijetí platných hodnot ve vašem prostředí.

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>Řádky cesty pro nákupní objednávky (ITMPurchaseLineEntity)

Řádek cesty představuje jeden řádek nákupní objednávky, která je zahrnuta do cesty. Tento vztah je navázán prostřednictvím polí **Číslo nákupní objednávky** a **Číslo řádku nákupu**. Řádek cesty odkazuje na každý předchozí záznam, který byl vytvořen pro cestu, přepravní kontejner a folio. Tato funkce je podporována entitou `ITMPurchaseLineEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Měna | ITMLine.CurrencyCode | Nvarchar(3) | Číslo | Číslo |
| Čistá částka | ITMLine.LineAmountMST | Numeric(32, 6) | Číslo | Číslo |
| Číslo řádku nákupu | ITMLine.RefRecId | Numeric(32, 6) | **Ano** | Číslo |
| Přepravní kontejner | ITMLine.ShipContainerId | Int | Číslo | Číslo |
| Společnost | ITMLine.ShipDataArea | Nvarchar(20) | **Ano** | Číslo |
| Deklarované množství | ITMLine.ShipDeclaredQty | Nvarchar(4) | Číslo | Číslo |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Číslo | Číslo |
| Cesta | ITMLine.ShipId | Nvarchar(20) | **Ano** | Číslo |
| Číslo položky | ITMLine.ShipItemId | Nvarchar(20) | Číslo | Číslo |
| Měrný systém | ITMLine.ShipMeasurement | Nvarchar(20) | Číslo | Číslo |
| Měrná jednotka | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Číslo | Číslo |
| Počet kartonů | ITMLine.ShipNoOfCartons | Int | Číslo | Číslo |
| Pozice | ITMLine.ShipPosition | Numeric(32, 6) | Číslo | Číslo |
| Množství | ITMLine.ShipQty | Int | Číslo | Číslo |
| Číslo nákupní objednávky | ITMline.TransRefId | Numeric(32, 6) | **Ano** | Číslo |
| Jednotka | ITMLine.UnitId | Int | Číslo | Číslo |
| Objem | ITMLine.Volume | Nvarchar(10) | Číslo | Číslo |
| Váha | ITMLine.Weight | Numeric(32, 6) | Číslo | Číslo |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>Řádky cesty pro převodní příkazy (ITMTransferLineEntity)

Řádek cesty představuje jeden řádek převodního příkazu, který je zahrnut do cesty. Tento vztah je navázán prostřednictvím polí **Číslo převodního příkazu** a **Číslo řádku převodu**. Řádek cesty odkazuje na každý předchozí záznam, který byl vytvořen pro cestu, přepravní kontejner a folio. Tato funkce je podporována entitou `ITMTransferLineEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Měna | ITMLine.CurrencyCode | Nvarchar(3) | Číslo | Číslo |
| Čistá částka | ITMLine.LineAmountMST | Numeric(32, 6) | Číslo | Číslo |
| Přepravní kontejner | ITMLine.ShipContainerId | Int | Číslo | Číslo |
| Společnost | ITMLine.ShipDataArea | Nvarchar(20) | **Ano** | Číslo |
| Deklarované množství | ITMLine.ShipDeclaredQty | Nvarchar(4) | Číslo | Číslo |
| Folio | ITMLine.ShipFolioId | Numeric(32, 6) | Číslo | Číslo |
| Cesta | ITMLine.ShipId | Nvarchar(20) | **Ano** | Číslo |
| Číslo položky | ITMLine.ShipItemId | Nvarchar(20) | Číslo | Číslo |
| Měrný systém | ITMLine.ShipMeasurement | Nvarchar(20) | Číslo | Číslo |
| Měrná jednotka | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | Číslo | Číslo |
| Počet kartonů | ITMLine.ShipNoOfCartons | Int | Číslo | Číslo |
| Pozice | ITMLine.ShipPosition | Numeric(32, 6) | Číslo | Číslo |
| Množství | ITMLine.ShipQty | Int | Číslo | Číslo |
| Číslo řádku převodu | ITMLine.TransferLineNumber | Numeric(32, 6) | **Ano** | Číslo |
| Číslo převodního příkazu | ITMline.TransRefId | Numeric(32, 6) | **Ano** | Číslo |
| Jednotka | ITMLine.UnitId | Int | Číslo | Číslo |
| Objem | ITMLine.Volume | Nvarchar(10) | Číslo | Číslo |
| Váha | ITMLine.Weight | Numeric(32, 6) | Číslo | Číslo |

### <a name="reference-table"></a>Referenční tabulka

Řádky cesty jsou vytvářeny prostřednictvím asociace s řádkem otevřené příchozí objednávky. Tento řádek může být na nákupní objednávce nebo to může být transakce příjmu na převodním příkazu. Pole `RefTableId` v tabulce řádků cesty (`ITMLine`) určuje, ke kterému typu objednávky se řádek vztahuje, a to odkazem na číslo tabulky. Pokud se v tabulce, kde se vytvářejí data, odkazují na konkrétní čísla tabulek, entity se rozdělí na základě těchto hodnot.

Hodnoty pro referenční tabulku (`RefTableId`) a typ transakce (`TransType`) jsou implicitní ve výběru entity nákupního řádku nákladů za doručení nebo entity řádku převodu nákladů za doručení.

### <a name="validation"></a>Ověření

Řádek cesty přímo odkazuje na záznam cesty, záznam přepravního kontejneru a záznam folia. Pokud se entita nákupního řádku (`ITMPurchaseLinesEntity`) nebo entita řádku převodu (`ITMPurchaseLinesEntity`) používá nezávisle na entitách používaných k vytvoření těchto referenčních záznamů, hodnoty **ID cesty** (`ShipId`), **Přepravní kontejner** (`ShipContainerId`) a **Folio** (`ShipFolioId`) musejí odpovídat existujícímu záznamu v odpovídajících tabulkách. V opačném případě se import nezdaří.

Pokud je kterákoli entita řádku použita jako součást stejné relace importu, musí tyto další entity předcházet vytvoření řádku cesty. V opačném případě nelze hodnoty úspěšně ověřit. Pokud je pro číslo cesty nebo folia použita zástupná hodnota, lze asociaci vytvořit pouze v případě, že je použit stejný zástupný symbol jako číslo cesty nebo folia v entitě řádku cesty.

Pokud je řádek nákupní objednávky nebo převodního příkazu již přiřazen k existujícímu řádku cesty, nová trasa se nevytvoří. Než bude možné přiřadit řádek objednávky k nové cestě, musí být odstraněn ze své aktuální cesty.

### <a name="order-line-identification"></a>Identifikace řádku objednávky

Řádky cesty přímo odkazují na referenční hodnoty **ID záznamu** (`RefRecId`), **ID dimenze zásob** (`InventDimId`) a **ID transakce zásob** (`InventTransId`). Tyto hodnoty již nemusí být zahrnuty při použití datové entity. Místo toho musí být nyní zahrnuto číslo řádku objednávky. Číslo řádku objednávky a číslo objednávky společně umožňují identifikovat každou z těchto referenčních hodnot.

### <a name="voyage-line-quantity"></a>Množství řádku cesty

Protože řádek cesty je přímo asociován s řádkem objednávky, hodnota **Množství** (`ShipQty`) zadaná pomocí entity vyžaduje, aby se hodnoty shodovaly. Ověření probíhá vůči množství buď na řádku nákupní objednávky, nebo na řádku převodu. Pokud se ověření nezdaří, záznam nebude zpracován.

### <a name="calculated-fields"></a>Kalkulovaná pole

Vypočítaná pole **Hmotnost** a **Objem** přijímají hodnoty, které jsou přijímány prostřednictvím datové entity. Pokud nejsou zadány žádné hodnoty, použijí se k aktualizaci těchto polí systémové hodnoty, pokud jsou dostupné. U nákladů za doručení se hodnoty vypočítají následujícím způsobem:

- *Hmotnost* = *Množství* × *Hrubá hmotnost položky*
- *Objem* = *Množství* × (*Celková hloubka položky* × *Celková výška položky* × *Celková šířka položky*)

## <a name="sequencing"></a>Klasifikace

Kvůli závislostem mezi tabulkami musí být nejprve vytvořen záznam o cestě. Řádek cesty lze vytvořit až po vytvoření cesty, přepravního kontejneru a folií.

Chcete-li vytvořit cestu bez upozornění na ověření, musí systém zpracovat entity v následujícím pořadí:

1. Cesty (`ITMTableEntity`)
1. Přepravní kontejnery (`ITMContainersEntity`)
1. Folia (`ITMFolioTableEntity`)
1. Řádky cesty (`ITMPurchaseLinesEntity` nebo `ITMTransferLinesEntity`)
