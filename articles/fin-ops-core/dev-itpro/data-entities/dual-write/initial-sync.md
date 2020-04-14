---
title: Řetězec závislosti entity (pořadí synchronizace)
description: Toto téma popisuje pořadí synchronizace, které je nutné provést při vytváření počátečních dat.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 4adb2c8d57ad8f67346b8d34212b7a4b0bd052ab
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173124"
---
# <a name="entity-dependency-chain-synchronization-order"></a>Řetězec závislosti entity (pořadí synchronizace)

[!include [banner](../../includes/banner.md)]



V následujících tabulkách jsou uvedeny entity v pořadí, v jakém byste je měli povolit. Když povolíte mapu pro počáteční synchronizaci, dvojitý zápis automaticky rozpozná ostatní mapy, které je nutné povolit. Stránku **Dvojitý zápis** v aplikacích Finance and Operations můžete použít k výběru nebo zrušení výběru entit během počáteční synchronizace.

V nejnovější verzi dvojitého zápisu lze povolit pouze některé entity a o závislosti je pro vás postaráno.

## <a name="dynamics-365-supply-chain-management-entities"></a>Entity Dynamics 365 Supply Chain Management

Následující entity pro Supply Chain Management jsou uvedeny v pořadí, v jakém byste je měli povolit.

| Název mapování na stránce dvojího zápisu | Název metadat entity v modulu Supply Chain Management | Název metadat entity v Common Data Service | Poznámky |
|---|---|---|---|
| Jednotky ... uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| Převody jednotek ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| Všechny produkty ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| Skupiny dimenzí produktu ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| Skupiny dimenze úložiště ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| Skupiny sledovací dimenze ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| Barvy ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| Velikosti ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| Styly ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| Konfigurace ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| Uvolněné produkty V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Uvolněné jedinečné produkty Common Data Service ... products                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | produkt                                      | |
| Čárový kód identifikovaný číslem produktu ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| Výchozí nastavení objednávky ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| Výchozí nastavení pořadí produktů V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| Převody jednotek pro určité produkty ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| Pracoviště ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| Sklady ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | Viz [poznámka 1](#scm-notes). |
| Barvy základního produktu ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| Velikosti základního produktu ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| Styly základního produktu ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| Konfigurace základního produktu ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| Kategorie produktů ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | Viz [poznámka 2](#scm-notes). |
| Přiřazení kategorií produktů ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| Hierarchie kategorií produktů ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| Role hierarchie kategorií produktů ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| Skladová ulička ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| Zóny skladu ... msdyn_warehouses                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| Skupiny zón skladu ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| Skladová místa ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | Viz [poznámka 3](#scm-notes). |
| Záhlaví práce ve skladu ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| Řádky práce ve skladu ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | Viz [poznámka 4](#scm-notes). |
| Způsoby dodání ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| Dodací podmínky ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| Kódy původních prodejních objednávek ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Záhlaví prodejní objednávky Common Data Service... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Řádky prodejní objednávky Common Data Service ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Záhlaví prodejní nabídky Common Data Service ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | nabídka                                        | |
| Řádky prodejní nabídky Common Data Service ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| Záhlaví prodejní faktury V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | faktura                                      | |
| Řádky prodejní faktury V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>Poznámky k mapování

1. Vzhledem k samoobslužné povaze možná budete muset dvakrát spustit počáteční synchronizaci.
2. Ve výchozím nastavení je počáteční synchronizace vypnuta z důvodu vztahu nadřazený–podřízený („inteligentní“ řazení platforma nepodporuje). Proto je nutné, aby byly existující kategorie produktů ručně synchronizovány (například aktualizací popisu kategorie) ve správném pořadí (nejprve kořenová kategorie, pak podřízené položky a poté podřízené položky podřízených položek). Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Kategorie a atributy \> Hierarchie kategorií**. Na stránce **Hierarchie kategorií** můžete vybrat každou hierarchii a zobrazit v ní kategorie produktů.
3. Mapování prázdných vyhledávacích polí **ItemNumberInLocation** a první, druhé a třetí dodatečné zóny skladu způsobí selhání počáteční synchronizace. Proto jsou tato mapování momentálně odebrána.
4. Mapování prázdného pole **CaptureWeight** způsobí, že počáteční synchronizace selže. Proto je tohle mapování momentálně odebráno.

### <a name="setup-related-information"></a>Informace související s nastavením

+ Když jsou záznamy nejprve vytvořeny v entitě **Produkty** v modelem řízených aplikacích Dynamics 365, mají stav **Koncept**. Chcete-li změnit stav na **Aktivní**, v modelem řízené aplikaci přejděte k **Nastavení \> Správa \> Nastavení systému \> Prodej** a nastavte možnost **Vytvořit produkty v aktivním stavu** na hodnotu **Ano**.
+ Vytváříte-li záznamy v entitě **Produkty** v modelem řízených aplikacích Dynamics 365 nebo Common Data Service, než povolíte dvojitý zápis, budou tyto záznamy aktualizovány pouze v případě, že celý klíč včetně entity **Společnost** odpovídá datům v aplikaci Finance and Operations.
+ Synchronizace entity **Produkty** je jednosměrný, z aplikací Finance and Operations do Common Data Service. Pokud je mapované pole v entitě **Produkty** v modelem řízených aplikacích Dynamics 365 aktualizováno, aktualizace bude přepsána během následující synchronizace z aplikace Finance and Operations.

### <a name="known-issues"></a>Známé problémy

- Při odstranění jednotky v aplikaci Finance and Operations dojde k chybě. Když se měrné jednotky synchronizují z aplikace Finance and Operations do Common Data Service, bude vytvořena první jednotka specifické třídy jako primární jednotka a bude zabráněno jejímu odstranění.

    **Zmírnění:** Jednotku nejprve odstraňte v Common Data Service. Poté ji lze odstranit v aplikaci Finance and Operations.

- Při odstranění provozního pracoviště v Common Data Service dojde k chybě. Chybové zprávy jsou následující: „Informační protokol: Upozornění: primární adresu nelze odstranit.; Upozornění: záznam entity nelze odstranit, protože ověření následujícího zdroje dat se nezdařilo: InventSiteLogisticsLocation (InventSiteLogisticsLocation).“ Tato chyba je způsobena problémem v datové entitě aplikace Finance and Operations.

    **Zmírnění:** Pracoviště můžete odstranit v aplikaci Finance and Operations. Pracoviště bude poté odstraněno v Common Data Service, pokud je spuštěna odpovídající mapa dvojitého zápisu.

## <a name="dynamics-365-finance-entities"></a>Entity Dynamics 365 Finance

Následující entity pro Dynamics 365 Finance jsou uvedeny v pořadí, v jakém byste je měli povolit.

| Název mapování na stránce dvojího zápisu | Název metadat entity ve Finance | Název metadat entity v Common Data Service | Poznámky |
|---|---|---|---|
| Měny ... transactioncurrencies                                            | CurrencyEntity                              | Měna                                   | |
| Typ směnného kurzu ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| Pár měny směnného kurzu ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Směnné kurzy Common Data Service ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | Viz [poznámka 1](#fin-notes). |
| Entita integrace fiskálního kalendáře ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| Entita integrace roku fiskálního kalendáře ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| Období fiskálního kalendáře ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| Typ organizační hierarchie ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | Viz [poznámka 1](#fin-notes). |
| Účely organizační hierarchie ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | Viz [poznámka 1](#fin-notes). |
| Právnické osoby ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | Viz [poznámka 1](#fin-notes). |
| Právnické osoby ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| Provozní jednotka ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | Viz [poznámka 1](#fin-notes). |
| Organizační hierarchie – publikována ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | Viz [poznámka 1](#fin-notes). |
| Přípony názvu ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| Platební dny Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| Řádky platebních dnů Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| Platební kalendář ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| Řádky platebního kalendáře ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| Platební podmínky ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| Způsob platby odběratele ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| Způsob platby dodavatele ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| Skupiny zákazníků ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| Skupiny dodavatelů ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| Skupiny DPH ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| Skupiny DPH položky ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| Účetní skupiny hlavní knihy pro DPH V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| Entita kódu osvobození od DPH Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| Finanční úřady ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| Kód DPH ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | Viz [poznámka 1](#fin-notes). |
| Formát finanční dimenze ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| Finanční dimenze ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| Skupiny srážkové daně ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| Kódy srážkové daně ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| Účtová osnova ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| Hlavní kniha ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | Viz [poznámka 1](#fin-notes). |
| Kategorie hlavního účtu ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| Hlavní účet ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| Zákazníci V3 ... accounts                                                       | CustCustomerV3Entity                        | účet                                    | Viz [poznámka 2](#fin-notes). |
| Zákazníci V3 ... contacts                                                       | CustCustomerV3Entity                        | kontaktovat                                    | Viz [poznámka 3](#fin-notes). |
| Dodavatelé V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | Viz [poznámka 2](#fin-notes). |
| Common Data Service kontakty V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | kontaktovat                                    | Viz [poznámka 4](#fin-notes). |
| Common Data Service kontakty V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | kontaktovat                                    | Viz [poznámka 5](#fin-notes). |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>Poznámky k mapování

1. Jednosměrná synchronizace je prováděna z aplikací Finance and Operations do Common Data Service.
2. Vzhledem k samoobslužné povaze možná budete muset vícekrát spustit počáteční synchronizaci. Při vytváření účtu na stránce **Účty** v Common Data Service je třeba jako typ vztahu vybrat **Zákazník**. Pokud při počáteční synchronizaci dojde k potížím s polem **Primární kontakt**, odeberte toto pole z mapování a spusťte znovu počáteční synchronizaci. Po úspěšném dokončení počáteční synchronizace zastavte mapování a znovu přidejte pole **Primární kontakt**. Poté spusťte mapování, ale vynechejte počáteční synchronizaci. Hodnota pole **Primární kontakt** nebude zahrnuta do počáteční synchronizace a je nutné hodnoty ručně migrovat.
3. Při pokusu o vytvoření zákazníka typu **Osoba** se ujistěte, že jste v Common Data Service na stránce **Kontakty** nastavili možnost **Prodejné** na hodnotu **Ano**.
4. Toto mapování má filtr na obou stranách, aby bylo možné propojit kontakty zákazníka. Otevřete podrobnosti mapování, vyberte tlačítko filtru (symbol trychtýře) vedle názvu entity **Sales.Contact** a zkontrolujte, zda kritéria filtru obsahují **msdyn_contactforvendor eq true and msdyn_sellable eq false**.
5. Toto mapování má filtr na obou stranách, aby bylo možné propojit kontakty dodavatele. Otevřete podrobnosti mapování, vyberte tlačítko filtru (symbol trychtýře) vedle názvu entity **Sales.Contact** a zkontrolujte, zda kritéria filtru obsahují **msdyn_contactforvendor eq true and msdyn_sellable eq false**. 

## <a name="dynamics-365-human-resources-entities"></a>Entity Dynamics 365 Human Resources

Následující entity pro Dynamics 365 Human Resources jsou uvedeny v pořadí, v jakém byste je měli povolit.

| Název mapování na stránce dvojího zápisu | Název metadat entity v modulu Human Resources | Název metadat entity v Common Data Service | Poznámky |
|---|---|---|---|
| cdm_jobfunction – pracovní funkce                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes – typy práce                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs – práce                                               |                                   | cdm_jobs                         | |
| cdm_jobs – podrobnosti práce                                        |                                   | cdm_jobs                         | |
| cdm_positiontype – typ pozice                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions – základní pozice                              | HcmPositionBaseEntity             | cdm_jobposition                  | Viz [poznámka 1](#hr-notes). |
| cdm_jobposition – podrobnosti pozice                            | HcmPositionDetailEntity           | cdm_jobposition                  | Viz [poznámka 1](#hr-notes). |
| cdm_jobposition – doba trvání pozice                           | HcmPositionDurationEntity         | cdm_jobposition                  | Viz [poznámka 1](#hr-notes). |
| cdm_jobposition – hierarchie pozic                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | Viz [poznámka 1](#hr-notes). |
| cdm_veteranstatus – statut veterána                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin – etnický původ                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode – kód jazyka                              |                                   | cdm_languagecode                 | |
| cdm_worker – pracovník                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments – zaměstnání                                 |                                   | cdm_employments                  | |
| cdm_employments – podrobnosti o zaměstnání                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps – přiřazení pracovníka k pozici | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | Viz [poznámka 2](#hr-notes).|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>Poznámky k mapování

1. Jedna entita Common Data Service je mapována na několik entit aplikace Finance and Operations.
2. Toto mapování má odkaz na sebe sama.

## <a name="asset-management-entities"></a>Entity správy majetku

Následující entity správy majetku pro Dynamics 365 Supply Chain Management jsou uvedeny v pořadí, v jakém byste je měli povolit.

| Název mapování na stránce dvojího zápisu | Název metadat entity ve správě majetku | Název metadat entity v Common Data Service | Poznámky |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | Správa majetku – stavy životního cyklu majetku               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | Správa majetku – modely životního cyklu majetku               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | Správa majetku – funkční místa – modely životního cyklu | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | Správa majetku – funkční místa – stavy životního cyklu | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | Správa majetku – typy majetku                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | Správa majetku – typy funkčních míst            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | Správa majetku – funkční místa                 | msdyn_functionallocations                | Viz [poznámka](#am-notes). |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | Správa majetku – majetek                               | msdyn_customerassets                     | Viz [poznámka](#am-notes). |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | Správa majetku – výrobci                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | Správa majetku – modely                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | Správa majetku – záruka                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>Poznámky k mapování

- Vzhledem k samoobslužné povaze možná budete muset vícekrát spustit počáteční synchronizaci.
