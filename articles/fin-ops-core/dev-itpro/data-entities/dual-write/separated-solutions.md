---
title: Oddělený balíček pro orchestraci aplikace s duálním zápisem
description: Balíček pro orchestraci aplikace s duálním zápisem již není jediným balíčkem, ale byl rozdělen do menších balíčků. Tento článek popisuje řešení a mapy, které každý balíček obsahuje, a jeho závislost na jiných balíčcích.
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 28c321ee2815b2886c07bfb0996870e536458145
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111653"
---
# <a name="separated-dual-write-application-orchestration-package"></a>Oddělený balíček pro orchestraci aplikace s duálním zápisem

[!include [banner](../../includes/banner.md)]



Dříve byl balíček pro orchestraci aplikace s duálním zápisem jediný balíček, který obsahoval následující řešení:

- Dynamics 365 – poznámky
- Dynamics 365 finance a provoz – společná kotva
- Dynamics 365 finance a provoz – mapy entit s dvojím zápisem
- Aplikace Dynamics 365 – správa majetku
- Dynamics 365 – správa majetku
- Společné HCM
- Dynamics 365 – rozšířený dodavatelský řetězec
- Dynamics 365 Finance Extended
- Dynamics 365 finance a provoz – společné
- Dynamics 365 – společnost
- Směnné kurzy měny
- Field Service Common

Protože se jednalo o jediný balíček, zákazníky stavěl do situace „vše nebo nic“. Microsoft jej však nyní rozdělil do menších balíčků. Zákazníci si tak mohou vybrat pouze balíčky pro řešení, které potřebují. Pokud jste například zákazník Microsoft Dynamics 365 Supply Chain Management a nepotřebujete integraci s Dynamics 365 Human Resources, poznámky a správu majetku, můžete tato řešení vyloučit z nainstalovaných řešení. Vzhledem k tomu, že základní názvy řešení, vydavatel a verze map zůstávají stejné, tato změna nemá na nic vliv. Stávající instalace budou upgradovány.

![Oddělený balíček.](media/separated-package-1.png)

Tento článek popisuje řešení a mapy, které každý balíček obsahuje, a jeho závislost na jiných balíčcích.

## <a name="dual-write-application-core"></a>Základ aplikace s duálním zápisem

Balíček Základ aplikace s duálním zápisem umožňuje uživatelům instalovat a konfigurovat duální zápis bez jakékoli aplikace pro zapojení zákazníků. Obsahuje následujících pět řešení:

| Jedinečný název                           | Zobrazovaný název                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 – společnost                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations - společné |
| CurrencyExchangeRates                 | Směnné kurzy měny                    |
| msdyn_DualWriteAppCoreMaps            | Základní mapy entit aplikací s duálním zápisem   |
| msdyn_DualWriteAppCoreAnchor          | Základní kotva aplikací s duálním zápisem        |

K dispozici pro tento balíček jsou následující mapy.

| Finanční a provozní aplikace     | Aplikace Customer Engagement                    |
|---------------------------------|---------------------------------------------|
| Provozní jednotka                  | msdyn_internalorganizations                 |
| Organizační hierarchie          | msdyn_internalorganizationhierarchies       |
| Právnické osoby                  | msdyn_internalorganizations                 |
| Právnické osoby                  | cdm_companies                               |
| Účely organizační hierarchie | msdyn_internalorganizationhierarchypurposes |
| Pár měny směnného kurzu     | msdyn_currencyexchangeratepairs             |
| Přípony názvu                    | msdyn_nameaffixes                           |
| Typ směnného kurzu              | msdyn_exchangeratetypes                     |
| Směnné kurzy CDS              | msdyn_currencyexchangerates                 |
| Typ organizační hierarchie     | msdyn_internalorganizationhierarchytypes    |
| Měny                      | transactioncurrencies                       |
| Entita průvodců využívajících hybridní realitu     | msmrw_guides                                |

**Informace o závislostech**

Balíček Základ aplikace s duálním zápisem není závislý na jiných balíčcích.

## <a name="dual-write-human-resources"></a>Lidské zdroje s duálním zápisem

Balíček Lidské zdroje s duálním zápisem obsahuje řešení a mapy, které jsou nutné k synchronizaci dat z Human Resources. Obsahuje následující tři řešení:

| Jedinečný název                | Zobrazovaný název                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | Společné HCM                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources – mapy entit |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources – kotva      |

K dispozici pro tento balíček jsou následující mapy.

| Finanční a provozní aplikace | Aplikace Customer Engagement         |
|-----------------------------|----------------------------------|
| Etnický původ              | cdm_ethnicorigins                |
| Pracovní funkce kompenzace   | cdm_jobfunctions                 |
| Pozice V2                | cdm_jobpositions                 |
| Práce                        | cdm_jobs                         |
| Typ práce kompenzace       | cdm_jobtypes                     |
| Kódy jazyka              | cdm_languages                    |
| Typ pozice               | cdm_positiontypes                |
| Přiřazení pracovníků k pozici | cdm_positionworkerassignmentmaps |
| Statut veterána              | cdm_veteranstatuses              |
| Pracovní podproces                      | cdm_workers                      |
| Zaměstnání podle společnosti      | cdm_employments                  |

**Informace o závislostech**

Balíček Lidské zdroje s duálním zápisem závisí na balíčku Základní aplikace s duálním zápisem. Proto byste měli nainstalovat balíček Základ aplikace s duálním zápisem před instalací balíčku Lidské zdroje s duálním zápisem.

## <a name="dual-write-supply-chain"></a>Dodavatelský řetězec s duálním zápisem

Balíček Dodavatelský řezěuec s duálním zápisem obsahuje řešení a mapy, které jsou nutné k synchronizaci dat ze Supply Chain Management. Obsahuje následující tři řešení:

| Jedinečný název                                | Zobrazovaný název                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 – rozšířený dodavatelský řetězec                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management – rozšířené mapy entit |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management – rozšířená kotva      |

K dispozici pro tento balíček jsou následující mapy.

| Finanční a provozní aplikace                 | Aplikace Customer Engagement                      |
|---------------------------------------------|-----------------------------------------------|
| Jednotky                                       | uoms                                          |
| Záhlaví prodejní objednávky CDS                     | salesorders                                   |
| Řádky prodejní objednávky CDS                       | salesorderdetails                             |
| Záhlaví prodejní nabídky CDS                  | nabídky                                        |
| Řádky prodejní nabídky CDS                   | quotedetails                                  |
| Uvolněné jedinečné produkty CDS              | produkty                                      |
| Zóny skladu                             | msdyn_warehousezones                          |
| Skupiny zón skladu                       | msdyn_warehousezonegroups                     |
| Řádky práce skladu                        | msdyn_warehouseworklines                      |
| Záhlaví práce skladu                      | msdyn_warehouseworkheaders                    |
| Sklady                                  | msdyn_warehouses                              |
| Skladová ulička                             | msdyn_warehouseaisles                         |
| Převody jednotek                            | msdyn_unitofmeasureconversions                |
| Dodací podmínky                           | msdyn_termsofdeliveries                       |
| Způsoby dodání                           | msdyn_shipvias                                |
| Styly základního produktu                       | msdyn_sharedproductstyles                     |
| Řádky prodejní faktury V2                      | invoicedetails                                |
| Záhlaví prodejní faktury V2                    | faktury                                      |
| Velikosti základního produktu                        | msdyn_sharedproductsizes                      |
| Uvolněné produkty V2                        | msdyn_sharedproductdetails                    |
| Konfigurace základního produktu               | msdyn_sharedproductconfigurations             |
| Barvy základního produktu                       | msdyn_sharedproductcolors                     |
| Kódy původu prodejních objednávek                    | msdyn_salesorderorigins                       |
| Záhlaví příjemky produktů                      | msdyn_purchaseorderreceipts                   |
| Řádek příjemky produktu                        | msdyn_purchaseorderreceiptproducts            |
| Záhlaví nákupní objednávky V2                   | msdyn_purchaseorders                          |
| Obnovitelně odstraněná entita řádku nákupní objednávky CDS | msdyn_purchaseorderproducts                   |
| Entita řádku nákupní objednávky CDS              | msdyn_purchaseorderproducts                   |
| Skupiny sledovací dimenze                   | msdyn_producttrackingdimensiongroups          |
| Styly                                      | msdyn_productstyles                           |
| Skupiny dimenze úložiště                    | msdyn_productstoragedimensiongroups           |
| Převody jednotek pro určité produkty           | msdyn_productspecificunitofmeasureconversions |
| Výchozí nastavení pořadí produktů V2           | msdyn_productspecificdefaultordersettings     |
| Velikosti                                       | msdyn_productsizes                            |
| Skupiny dimenzí produktu                    | msdyn_productdimensiongroups                  |
| Výchozí nastavení objednávky                      | msdyn_productdefaultordersettings             |
| Konfigurace                              | msdyn_productconfigurations                   |
| Všechny výrobky                                | msdyn_globalproducts                          |
| Barvy                                      | msdyn_productcolors                           |
| Role hierarchie kategorií produktů            | msdyn_productcategoryhierarchyroles           |
| Hierarchie kategorií produktů                | msdyn_productcategoryhierarchies              |
| Přiřazení kategorií produktů                | msdyn_productcategoryassignments              |
| Kategorie produktu                          | msdyn_productcategories                       |
| Skladová místa ve skladu                         | msdyn_inventorylocations                      |
| Zásoby CDS v                            | msdyn_inventoryonhandentries                  |
| Kategorie produktu                          | msdyn_productcategories                       |
| Zásoby CDS v                            | msdyn_inventoryonhandrequests                 |
| Identifikované čárové kódy čísla produktu           | msdyn_productbarcodes                         |
| Věrnostní karta                                | msdyn_loyaltycards                            |
| Body věrnostní odměny                       | msdyn_loyaltyrewardpoints                     |
| Skupiny odběratelů cen                       | msdyn_pricecustomergroups                     |
| Pracoviště                                       | msdyn_operationalsites                        |
| Řádky prodejní nabídky CDS                   | quotedetails                                  |
| Řádky prodejní objednávky CDS                       | salesorderdetails                             |

**Informace o závislostech**

Balíček Dodavatelský řetězec s duálním zápisem závisí na následujících třech balíčcích. Proto byste měli nainstalovat tyto balíčky před instalací balíčku Dodavatelský řetězec s duálním zápisem.

- Balíček Základ aplikace s duálním zápisem
- Balíček Finance s duálním zápisem
- Balíček Lidské zdroje s duálním zápisem

## <a name="dual-write-finance"></a>Finance s duálním zápisem

Balíček Finance s duálním zápisem obsahuje řešení a mapy, které jsou nutné k synchronizaci dat z Dynamics 365 Finance. Obsahuje následujících čtyři řešení.

| Jedinečný název                            | Zobrazovaný název                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Mapy entit Dynamics 365 Finance extended |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Kotva Dynamics 365 Finance extended      |

K dispozici pro tento balíček jsou následující mapy.

| Finanční a provozní aplikace             | Aplikace Customer Engagement        |
|-----------------------------------------|---------------------------------|
| Skupiny srážkové daně                  | msdyn_withholdingtaxgroups      |
| CDS Contacts V2 (zákazník)              | kontakty                        |
| CDS Contacts V2 (dodavatel)                | kontakty                        |
| Zákazníci V3                            | kontakty                        |
| Kódy srážkové daně                   | msdyn_withholdingtaxcodes       |
| Dodavatelé V2                              | msdyn_vendors                   |
| Platební metoda dodavatele                   | msdyn_vendorpaymentmethods      |
| Skupiny dodavatelů                           | msdyn_vendorgroups              |
| Účtová osnova                       | msdyn_chartofaccountses         |
| Účetní skupiny hlavní knihy pro DPH V2      | msdyn_taxpostinggroups          |
| Skupina DPH zboží                    | msdyn_taxitemgroups             |
| Skupiny DPH                        | msdyn_taxgroups                 |
| CDS entita kódu osvobození od DPH        | msdyn_taxexemptcodes            |
| Skupiny odběratelů                         | msdyn_customergroups            |
| Způsob platby odběratele                 | msdyn_customerpaymentmethods    |
| Finanční dimenze                    | msdyn_dimensionattributes       |
| Finanční úřady                   | msdyn_taxauthorities            |
| Formát finanční dimenze              | msdyn_financialdimensionformats |
| Fiskální kalendářní období                  | msdyn_fiscalcalendarperiods     |
| Entita integrace fiskálního kalendáře      | msdyn_fiscalcalendars           |
| Entita integrace roku fiskálního kalendáře | msdyn_fiscalcalendaryears       |
| Platební podmínky                        | msdyn_paymentterms              |
| Platební kalendář                        | msdyn_paymentschedules          |
| Řádky platebního kalendáře                  | msdyn_paymentschedulelines      |
| Dny platby CDS                        | msdyn_paymentdays               |
| Řádky dnů platby CDS V2                | msdyn_paymentdaylines           |
| Hlavní účet                            | msdyn_mainaccounts              |
| Kategorie hlavního účtu                 | msdyn_mainaccountcategories     |
| Ledger                                  | msdyn_ledgers                   |
| Zákazníci V3                            | účty                        |

**Informace o závislostech**

Balíček Finance s duálním zápisem závisí na balíčku Základní aplikace s duálním zápisem. Proto byste měli nainstalovat balíček Základ aplikace s duálním zápisem před instalací balíčku Finance s duálním zápisem.

## <a name="dual-write-notes"></a>Poznámky s duálním zápisem

Balíček Poznámky s duálním zápisem obsahuje řešení a mapy, které jsou nutné k synchronizaci dat poznámek nebo anotací. Obsahuje následujících čtyři řešení.

| Jedinečný název                  | Zobrazovaný název                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 – poznámky             |
| Dynamics365NotesExtended     | Dynamics 365 – rozšířené poznámky    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 – mapy entit poznámek |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 – kotva poznámek      |

K dispozici pro tento balíček jsou následující mapy.

| Finance a provoz                     | Customer Engagement |
|--------------------------------------------|---------------------|
| Přílohy dokumentu záhlaví prodejní objednávky    | anotace         |
| Přílohy zákazníků                       | anotace         |
| Přílohy dokumentu dodavatele                | anotace         |
| Přílohy dokumentu záhlaví nákupní objednávky | anotace         |

**Informace o závislostech**

Balíček Poznámky s duálním zápisem závisí na následujících dvou balíčcích. Proto byste měli nainstalovat tyto balíčky před instalací balíčku Poznámky s duálním zápisem.

- Balíček Základ aplikace s duálním zápisem
- Balíček Finance s duálním zápisem

## <a name="dual-write-asset-management"></a>Správa majetku s duálním zápisem

Balíček Správa majetku s duálním zápisem obsahuje řešení a mapy, které jsou nutné k synchronizaci dat majetku ze Supply Chain Management nebo Dynamics 365 Field Service. Obsahuje následujících čtyři řešení.

| Jedinečný název                          | Zobrazovaný název                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 – správa majetku             |
| Dynamics365AssetManagementApp        | Aplikace Dynamics 365 – správa majetku          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 – mapy entit správy majetku |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 – kotva správy majetku      |

K dispozici pro tento balíček jsou následující mapy.

| Finanční a provozní aplikace                           | Aplikace Customer Engagement                |
|-------------------------------------------------------|-----------------------------------------|
| Správa majetku – záruka                             | msdyn_warranties                        |
| Správa majetku – modely                               | msdyn_models                            |
| Správa majetku – výrobci                        | msdyn_manufacturers                     |
| Správa majetku – typy funkčních míst            | msdyn_functionallocationtypes           |
| Správa majetku – funkční místa                 | msdyn_functionallocations               |
| Správa majetku – funkční místa – stavy životního cyklu | msdyn_functionallocationlifecyclestates |
| Správa majetku – funkční místa – modely životního cyklu | msdyn_functionallocationlifecyclemodels |
| Správa majetku – majetek                               | msdyn_customerassets                    |
| Správa majetku – typy majetku                          | msdyn_customerassetcategories           |
| Správa majetku – stavy životního cyklu majetku               | msdyn_assetlifecyclestates              |
| Správa majetku – modely životního cyklu majetku               | msdyn_assetlifecyclemodels              |

**Informace o závislostech**

Balíček Správa majetku s duálním zápisem závisí na balíčku Základní aplikace s duálním zápisem. Proto byste měli nainstalovat balíček Základ aplikace s duálním zápisem před instalací balíčku Správa majetku s duálním zápisem.

## <a name="packages-required-for-project-operations"></a>Balíčky potřebné pro Project Operations
Project Operations závisí na následujících balíčcích. Proto byste měli nainstalovat tyto balíčky před instalací balíčku Project Operations.

- Balíček Základ aplikace s duálním zápisem
- Balíček Finance s duálním zápisem
- Balíček Dodavatelský řetězec s duálním zápisem
- Balíček Správa majetku s duálním zápisem
- Balíček Lidské zdroje s duálním zápisem

## <a name="dual-write-party-and-global-address-book-solutions"></a>Řešení strany a globálního adresáře s duálním zápisem

Balíček strany a globálního adresáře s duálním zápisem obsahuje následující řešení a mapy, které jsou nutné k synchronizaci dat stran a globálního adresáře. 

| Jedinečný název                       | Zobrazovaný název                            |
|-----------------------------------|-----------------------------------------|
| Strana                             | Strana                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB - rozšířené               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB – mapy entit s duálním zápisem |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB a strana              |

K dispozici pro tento balíček jsou následující mapy.

| Finanční a provozní aplikace | Aplikace Customer Engagement | 
|-----------------------------|--------------------------|
| Strany CDS | msdyn_parties | 
| Místa poštovní adresy CDS | msdyn_postaladdresscollections | 
| Historie poštovní adresy CDS V2 | msdyn_postaladdresses | 
| Místa poštovní adresy strany CDS | msdyn_partypostaladdresses | 
| Kontakty strany V3 | msdyn_partyelectronicaddresses | 
| Zákazníci V3 | účty | 
| Zákazníci V3 | kontakty | 
| Dodavatelé V2 | msdyn_vendors | 
| Tituly kontaktní osoby | msdyn_salescontactpersontitles | 
| Zdvořilostní zakončení | msdyn_complimentaryclosings | 
| Oslovení | msdyn_salutations | 
| Role v rozhodovacím procesu | msdyn_decisionmakingroles | 
| Pracovní funkce zaměstnání | msdyn_employmentjobfunctions | 
| Úrovně věrnosti | msdyn_loyaltylevels | 
| Typy osobní charakteristiky | msdyn_personalcharactertypes | 
| Kontakty V2 | msdyn_contactforparties | 
| Záhlaví prodejní nabídky CDS | nabídky | 
| Záhlaví prodejní objednávky CDS | salesorders | 
| Záhlaví prodejní faktury V2 | faktury | 
| Role adresy CDS | msdyn_addressroles |

**Informace o závislostech**

Řešení strany a globálního adresáře s dvojím zápisem závisí na následujících třech balíčcích. Proto byste měli nainstalovat tyto balíčky před instalací balíčku řešení strany a globálního adresáře s duálním zápisem.

- Balíček Základ aplikace s duálním zápisem
- Balíček Finance s duálním zápisem
- Balíček Dodavatelský řetězec s duálním zápisem

