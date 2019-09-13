---
title: Integrované sklady a pracoviště
description: Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service.
author: benebotg
manager: AnnBe
ms.date: 15/8/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 3ee5192138374c58df9f9cfc033503d200356771
ms.sourcegitcommit: 559637f30037f6b52ebc4d4c13d0ecec46d4a051
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/27/2019
ms.locfileid: "1920694"
---
# <a name="integrated-sites-and-warehouses"></a>Integrované sklady a pracoviště

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Toto téma popisuje integraci dat pracoviště a skladu mezi aplikacemi Finance and Operations a Common Data Service. Provozní pracoviště a sklady jsou obecnými koncepty v aplikaci správy dodavatelského řetězce. Používají se k modelování dodavatelského řetězce vaší společnosti.

## <a name="templates"></a>Šablony

Při integraci s aplikací Common Data Service jsou tyto koncepcy a všechny jeich souvisejíc informace k dispozic v Common Data Service pomocí datových entit pracovišť a skladů v následující tabulce.

Finance and Operations  | Aplikace Customer Engagement
--------------------------|---------------------------------
Weby                     | msdyn_operationalsites
Sklady                | sklady

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="operational-sites"></a>Provozní pracoviště

Provozní pracoviště jsou k dispozici v Common Data Service pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
SITENAME | >< | msdyn_name
DEFAULTFINANCIALDIMENSIONVALUE | >< | msdyn_defaultfinancialdimensionvalue
DEFAULTINVENTORYSTATUSID | >< | msdyn_defaultinventorystatusid
ISRECEIVINGWAREHOUSEOVERRIDEALLOWED | >< | msdyn_isreceivingwarehouseoverrideallowed
SITEID | >< | msdyn_siteid
SITENAME | >< | msdyn_sitename
TAXBRANCHCODE | >< | msdyn_taxbranchcode
FISCALESTABLISHMENTID | >< | msdyn_fiscalestablishmentid
ISPRIMARYADDRESSASSIGNED | >< | msdyn_isprimaryaddressassigned
PRIMARYADDRESSCITY | >< | msdyn_primaryaddresscity
PRIMARYADDRESSCOUNTRYREGIONID | >< | msdyn_primaryaddresscountryregionid
PRIMARYADDRESSCOUNTYID | >< | msdyn_primaryaddresscountyid
PRIMARYADDRESSDISTRICTNAME | >< | msdyn_primaryaddressdistrictname
PRIMARYADDRESSLATITUDE | >< | msdyn_primaryaddresslatitude
PRIMARYADDRESSLOCATIONROLES | >< | msdyn_primaryaddresslocationrole
PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE | >< | msdyn_primaryaddresslocationsalestaxgroupcode
PRIMARYADDRESSLONGITUDE | >< | msdyn_primaryaddresslongitude
PRIMARYADDRESSSTATEID | >< | msdyn_primaryaddressstateid
PRIMARYADDRESSSTREET | >< | msdyn_primaryaddressstreet
PRIMARYADDRESSZIPCODE | >< | msdyn_primaryaddresszipcode
PRIMARYADDRESSBUILDINGCOMPLIMENT | >< | msdyn_primaryaddressbuildingcompliment
PRIMARYADDRESSCITYINKANA | >< | msdyn_primaryaddresscityinkana
PRIMARYADDRESSSTREETINKANA | >< | msdyn_primaryaddressstreetinkana
PRIMARYADDRESSDESCRIPTION | >< | msdyn_primaryaddressdescription
FORMATTEDPRIMARYADDRESS | >< | msdyn_formattedprimaryaddress
WILLMASTERPLANNEDINTRASITEMOVEMENTSUSETRANSFERJOURNALS | >< | msdyn_masterplannedusestransferjournal
PRIMARYADDRESSPOSTBOX | >< | msdyn_primaryaddresspostbox
PRIMARYADDRESSSTREETNUMBER | >< | msdyn_primaryaddressstreetnumber


## <a name="warehouses"></a>Sklady

Sklady jsou k dispozici pomocí následujících mapování.

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
DEFAULTCONTAINERTYPEID | >> | msdyn_defaultcontainertypeid
AREITEMSCOVERAGEPLANNEDMANUALLY | >> | msdyn_areitemscoverageplannedmanually
ARELABORSTANDARDSALLOWED | >> | msdyn_arelaborstandardsallowed
PRIMARYADDRESSBUILDINGCOMPLIMENT | >> | msdyn_primaryaddressbuildingcompliment
PRIMARYADDRESSPOSTBOX | >> | msdyn_primaryaddresspostbox
PRIMARYADDRESSSTREETNUMBER | >> | msdyn_primaryaddressstreetnumber
AREWAREHOUSELOCATIONCHECKDIGITSUNIQUE | >> | msdyn_arewarehouselocationcheckdigitsunique
INVENTORYCOUNTINGREASONCODEPOLICYNAME | >> | msdyn_inventorycountingreasoncodepolicyname
AUTOUPDATESHIPMENTRULE | >> | msdyn_autoupdateshipmentrule
WAREHOUSERELEASERESERVATIONREQUIREMENTRULE | >> | msdyn_warehousereleasereservationrequirement
EXTERNALLYLOCATEDWAREHOUSEVENDORACCOUNTNUMBER | >> | msdyn_externallylocatedwarehousevendoraccountnu
INVENTORYSTATUSCHANGERESERVATIONREMOVALLEVEL | >> | msdyn_inventorystatuschangereservationremoval
WAREHOUSEWORKPROCESSINGPOLICYNAME | >> | msdyn_warehouseworkprocessingpolicyname
ISFALLBACKWAREHOUSE | >> | msdyn_isfallbackwarehouse
ISFINANCIALNEGATIVERETAILSTOREINVENTORYALLOWED | >> | msdyn_financialnegativestoreinventoryallowed
ISPALLETMOVEMENTDURINGCYCLECOUNTINGALLOWED | >> | msdyn_palletmovementduringcyclecountingallowed
ISPHYSICALNEGATIVERETAILSTOREINVENTORYALLOWED | >> | msdyn_physicalnegativestoreinventoryallowed
ISREFILLEDFROMMAINWAREHOUSE | >> | msdyn_isrefilledfrommainwarehouse
ISRETAILSTOREWAREHOUSE | >> | msdyn_isretailstorewarehouse
MAINREFILLINGWAREHOUSEID | >> | msdyn_mainrefillingwarehouseid.msdyn_warehouseid
MASTERPLANNINGWORKCALENDARDID | >> | msdyn_masterplanningworkcalendarid
MAXIMUMBATCHPICKINGLISTQUANTITY | >> | msdyn_maximumbatchpickinglistquantity
MAXIMUMPICKINGLISTLINEQUANTITY | >> | msdyn_maximumpickinglistlinequantity
OPERATIONALSITEID | >> | msdyn_operationalsiteid.msdyn_siteid
QUARANTINEWAREHOUSEID | >> | msdyn_quarantinewarehouseid.msdyn_warehouseid
RETAILSTOREQUANTITYALLOCATIONREPLENISMENTRULEWEIGHT | > | msdyn_storeqtyallocationreplenishmentweight
SHOULDWAREHOUSELOCATIONIDINCLUDEAISLEID | >> | msdyn_shouldwarehouselocationincludeaisleid
TRANSITWAREHOUSEID | >> | msdyn_transitwarehouseid.msdyn_warehouseid
WAREHOUSEID | >> | msdyn_warehouseid
WAREHOUSELOCATIONIDBINIDFORMAT | >> | msdyn_warehouselocationidbinidformat
WAREHOUSELOCATIONIDRACKIDFORMAT | >> | msdyn_warehouselocationidrackidformat
WAREHOUSELOCATIONIDSHELFIDFORMAT | >> | msdyn_warehouselocationidshelfidformat
WAREHOUSENAME | >> | msdyn_name
WAREHOUSENAME | >> | msdyn_warehousename
WAREHOUSESPECIFICDEFAULTINVENTORYSTATUSID | >> | msdyn_warehousespecificdefaultinventorystatusid
WAREHOUSETYPE | >> | msdyn_warehousetype
ISPRIMARYADDRESSASSIGNED | >> | msdyn_isprimaryaddressassigned
PRIMARYADDRESSCITY | >> | msdyn_primaryaddresscity
PRIMARYADDRESSCOUNTRYREGIONID | >> | msdyn_primaryaddresscountryregionid
PRIMARYADDRESSCOUNTYID | >> | msdyn_primaryaddresscountyid
PRIMARYADDRESSDISTRICTNAME | >> | msdyn_primaryaddressdistrictname
PRIMARYADDRESSLATITUDE | >> | msdyn_primaryaddresslatitude
PRIMARYADDRESSLONGITUDE | >> | msdyn_primaryaddresslongitude
PRIMARYADDRESSLOCATIONROLES | >> | msdyn_primaryaddresslocationroles
PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE | >> | msdyn_primaryaddresslocationsalestaxgroupcode
PRIMARYADDRESSSTATEID | >> | msdyn_primaryaddressstateid
PRIMARYADDRESSSTREET | >> | msdyn_primaryaddressstreet
PRIMARYADDRESSZIPCODE | >> | msdyn_primaryaddresszipcode
EXTERNALLYLOCATEDWAREHOUSECUSTOMERACCOUNTNUMBER | >> | msdyn_externallylocatedwarehousecustomeraccount
PRIMARYADDRESSCITYINKANA | >> | msdyn_primaryaddresscityinkana
PRIMARYADDRESSSTREETINKANA | >> | msdyn_primaryaddressstreetinkana
PRIMARYADDRESSDESCRIPTION | >> | msdyn_primaryaddressdescription
AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED | >> | msdyn_uesadvancedwarehousemanagementprocesses
AREPICKINGLISTSDELIVERYMODESPECIFIC | >> | msdyn_arepickinglistsdeliverymodespecific
AREPICKINGLISTSSHIPMENTSPECIFICONLY | >> | msdyn_arepickinglistshipmentspecificonly
FORMATTEDPRIMARYADDRESS | >> | msdyn_formattedprimaryaddress
ISBILLOFLADINGPRINTINGBEFORESHIPMENTCONFIRMATIONENABLED | >> | msdyn_printbillofladingbeforeshipconfirmation
RAWMATERIALPICKINGINVENTORYISSUESTATUS | >> | msdyn_rawmaterialpickinginventoryissuestatus
WILLAUTOMATICLOADRELEASERESERVEINVENTORY | >> | msdyn_willautomaticloadreleaseinventory
WILLINVENTORYSTATUSCHANGEREMOVEBLOCKING | >> | msdyn_willinventorystatuschangeremoveblocking
WILLMANUALLOADRELEASERESERVEINVENTORY | >> | msdyn_willmanualloadreleasereserveinventory
WILLORDERRELEASINGCONSOLIDATESHIPMENTS | >> | msdyn_willorderreleasingconsolidateshipments
WILLPRODUCTIONBOMSRESERVEWAREHOUSELEVELONLY | >> | msdyn_productionbomsreservewarehouselevel
WILLSHIPPINGCANCELLATIONDECREMENTLOADQUANITY | >> | msdyn_shippingcanceldecrementloadquantity
WILLWAREHOUSELOCATIONIDINCLUDEBINIDBYDEFAULT | >> | msdyn_warehouselocationidincludeblindid
WILLWAREHOUSELOCATIONIDINCLUDERACKIDBYDEFAULT | >> | msdyn_warehouselocationincluderackidbydefault
WILLWAREHOUSELOCATIONIDINCLUDESHELFIDBYDEFAULT | >> | msdyn_warehouselocationidincludeshelfid
