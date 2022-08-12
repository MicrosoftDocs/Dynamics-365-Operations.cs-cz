---
title: Entity nákladových transakcí
description: Tento článek poskytuje informace o entitách nákladových transakcí, které umožňují rozdělit hodnotu nákladů mezi obsah nákladové oblasti výběrem metody rozdělení.
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
ms.openlocfilehash: 0084d47bf85050749b2668d273db07670aaeae2a
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/15/2022
ms.locfileid: "9166796"
---
# <a name="cost-transaction-entities"></a>Entity nákladových transakcí

[!include [banner](../includes/banner.md)]

## <a name="apportionment"></a>Rozdělení nákladů

Náklady za doručení umožňují rozdělit hodnotu nákladů mezi obsah nákladové oblasti (cesta, přepravní kontejner atd.) prostřednictvím výběru metody rozdělení. Způsob rozdělení nákladů je nastaven jako součást konfigurace automatických nákladů, která je založena na obchodních pravidlech. Stane se součástí nákladů, když je vytvořen řádek cesty.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Konfigurace mapování rozdělení nákladů pro použití s datovými entitami

Když jsou náklady vytvořeny z externího zdroje, jako je speditér, tento externí zdroj nemůže určit preferovanou metodu pro rozdělení hodnoty nákladů. Mapování rozdělení nákladů definuje výchozí metodu rozdělení pro každý kód typu nákladů. Mapovací tabulka rozdělení nákladů je přístupná ze stránky **Mapování rozdělení nákladů** v aplikaci Microsoft Dynamics 365 Supply Chain Management (**Náklady za doručení\> Nastavení výpočtu nákladů \> Mapování rozdělení nákladů**).

Pokud byla definována kombinace mapování a náklady, které odpovídají kódu typu nákladů, jsou vytvořeny pomocí entity nákladové transakce, použije se metoda mapovaného rozdělení nákladů namísto jakékoli hodnoty, která byla entitě poskytnuta.

Pokud v mapovací tabulce není přítomna žádná hodnota, ale entitě hodnota zadána byla, použije se zadaná hodnota.

Pokud v mapovací tabulce ani v záznamu, který byl entitě odeslán, neexistuje žádná hodnota, vytvoření se nezdaří.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Mapování rozdělení nákladů (ITMApportionmentMapping)

Entita mapování rozdělení nákladů (`ITMApportionmentMapping`) vytváří vztahy mapování rozdělení nákladů a umožňuje uživatelům vytvářet nebo aktualizovat záznamy.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Způsob rozdělení | ITMApportionmentMapping.ApportionmentMethod | Int | Číslo | Číslo |
| Kód typu nákladů | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Ano** | Číslo |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Náklady na cestu (ITMCostTransVoyageEntity)

Jednotka nákladů na cestu (`ITMCostTransVoyageEntity`) vytváří transakce nákladů na cestu, které jsou aplikovány na úrovni cesty. Během procesu importu systém používá hodnoty **Kategorie** a **Metoda rozdělení**, které jsou součástí entity, aby se určilo, jak se hodnota nákladů rozdělí mezi obsah cesty.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Způsob rozdělení | ITMCostTrans.ApportionmentMethod | Int | Číslo | Číslo |
| Hodnota nákladů | ITMCostTrans.CostValue | Numeric(32, 6) | Číslo | Číslo |
| Měna | ITMCostTrans.CurrencyCode | Nvarchar(3) | Číslo | **Ano** |
| Číslo řádku | ITMCostTrans.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Propojený typ nákladů | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Minimální náklady | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Číslo | Číslo |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Číslo | Číslo |
| Kód typu nákladů | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Společnost | ITMCostTrans.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Cesta | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Skupina DPH zboží | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Číslo | Číslo |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Náklady na přepravní kontejner (ITMCostTransShippingContainerEntity)

Jednotka nákladů na přepravní kontejner (`ITMCostTransShippingContainerEntity`) vytváří náklady na přepravní kontejner, které se uplatňují na úrovni přepravního kontejneru. Během procesu importu systém používá hodnoty **Kategorie** a **Metoda rozdělení**, které jsou součástí entity, aby se určilo, jak se hodnota nákladů rozdělí mezi obsah přepravního kontejneru.

Pole **Agregovat**, **Úsek** a **Propojený úsek** jsou specifická pro záznamy, kde je **Oblast nákladů** nastavena na *Přepravní kontejner*. Proto nejsou přítomny v datových entitách pro jiné nákladové oblasti.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Agregovat | ITMCostTrans.AggregatedCost | Int | Číslo | Číslo |
| Způsob rozdělení | ITMCostTrans.ApportionmentMethod | Int | Číslo | Číslo |
| Hodnota nákladů | ITMCostTrans.CostValue | Numeric(32, 6) | Číslo | Číslo |
| Měna | ITMCostTrans.CurrencyCode | Nvarchar(3) | Číslo | **Ano** |
| Číslo řádku | ITMCostTrans.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Propojený typ nákladů | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Propojený úsek | ITMCostTrans.LinkLegId | Nvarchar(20) | Číslo | Číslo |
| Minimální náklady | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Číslo | Číslo |
| Přepravní kontejner | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Číslo | Číslo |
| Kód typu nákladů | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Společnost | ITMCostTrans.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Cesta | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Úsek | ITMCostTrans.ShipLegId | Nvarchar(20) | Číslo | Číslo |
| Skupina DPH zboží | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Číslo | Číslo |

## <a name="folio-costs-itmcosttransfolioentity"></a>Náklady folia (ITMCostTransFolioEntity)

Jednotka foliových nákladů (`ITMCostTransFolioEntity`) vytváří záznamy nákladových transakcí, které se vztahují na úroveň folia. Během procesu importu systém používá hodnoty **Kategorie** a **Metoda rozdělení**, které jsou součástí entity, aby se určilo, jak se hodnota nákladů rozdělí mezi obsah každého folia.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Způsob rozdělení | ITMCostTrans.ApportionmentMethod | Int | Číslo | Číslo |
| Hodnota nákladů | ITMCostTrans.CostValue | Numeric(32, 6) | Číslo | Číslo |
| Měna | ITMCostTrans.CurrencyCode | Nvarchar(3) | Číslo | **Ano** |
| Číslo řádku | ITMCostTrans.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Propojený typ nákladů | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Minimální náklady | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Číslo | Číslo |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Číslo | Číslo |
| Kód typu nákladů | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Společnost | ITMCostTrans.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Folio | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Skupina DPH zboží | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Číslo | Číslo |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Náklady na nákupní objednávku (ITMCostTransPurchaseEntity)

Nákladová entita nákupní objednávky (`ITMCostTransPurchaseEntity`) vytváří nákladové transakce, které se vztahují na hlavičku nákupní objednávky. Během procesu importu systém používá hodnoty **Kategorie** a **Metoda rozdělení**, které jsou součástí entity, aby se určilo, jak se hodnota nákladů rozdělí mezi obsah každého folia.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Způsob rozdělení | ITMCostTrans.ApportionmentMethod | Int | Číslo | Číslo |
| Hodnota nákladů | ITMCostTrans.CostValue | Numeric(32, 6) | Číslo | Číslo |
| Měna | ITMCostTrans.CurrencyCode | Nvarchar(3) | Číslo | **Ano** |
| Číslo řádku | ITMCostTrans.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Propojený typ nákladů | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Minimální náklady | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Číslo | Číslo |
| Nákupní objednávka | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Číslo | Číslo |
| Kód typu nákladů | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Společnost | ITMCostTrans.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Skupina DPH zboží | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Číslo | Číslo |

## <a name="item-costs-itmcosttransitementity"></a>Náklady na položku (ITMCostTransItemEntity)

Jednotka nákladů na položku (`ITMCostTransItemEntity`) vytváří nákladové transakce, které se vztahují na úroveň položky. Tato entita je specifická pro položky na řádcích nákupní objednávky. Hodnota nákladů se v plné výši aplikuje na řádek.

Pole **Částka úpravy** a **Úprava hodnoty** jsou specifická pro nákladové oblasti na úrovni řádku. Proto nejsou přítomny v datových entitách pro jiné nákladové oblasti.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Částka úpravy | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Číslo | Číslo |
| Hodnota nákladů | ITMCostTrans.CostValue | Numeric(32, 6) | Číslo | Číslo |
| Měna | ITMCostTrans.CurrencyCode | Nvarchar(3) | Číslo | **Ano** |
| Číslo řádku | ITMCostTrans.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Propojený typ nákladů | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Minimální náklady | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Číslo | Číslo |
| Nákupní objednávka | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Číslo řádku nákupní objednávky | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Číslo | Číslo |
| Kód typu nákladů | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Společnost | ITMCostTrans.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Skupina DPH zboží | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Číslo | Číslo |
| Úprava hodnoty | ITMCostTrans.ValueAdjustmentMethod | Int | Číslo | Číslo |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Náklady řádku převodu (ITMCostTransTransferLineEntity)

Entita nákladů řádku převodu (`ITMCostTransTransferLineEntity`) vytvoří nákladové transakce, které se vztahují na úroveň řádku převodního příkazu. Hodnota těchto nákladů se v plné výši aplikuje na řádek převodního příkazu.

Pole **Částka úpravy** a **Úprava hodnoty** jsou specifická pro nákladové oblasti na úrovni řádku. Proto nejsou přítomny v datových entitách pro jiné nákladové oblasti.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Částka úpravy | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | Číslo | Číslo |
| Hodnota nákladů | ITMCostTrans.CostValue | Numeric(32, 6) | Číslo | Číslo |
| Měna | ITMCostTrans.CurrencyCode | Nvarchar(3) | Číslo | **Ano** |
| Číslo řádku | ITMCostTrans.LineNum | Numeric(32, 16) | **Ano** | Číslo |
| Propojený typ nákladů | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Minimální náklady | ITMCostTrans.MinCostAmount | Numeric(32, 6) | Číslo | Číslo |
| Kategorie | ITMCostTrans.ShipCostCategory | Int | Číslo | Číslo |
| Kód typu nákladů | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | Číslo | Číslo |
| Společnost | ITMCostTrans.ShipDataArea | Nvarchar(4) | Číslo | **Ano** |
| Převodní příkaz | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Číslo řádku převodního příkazu | ITMCostTrans.TransRecId | Nvarchar(20) | **Ano** | Číslo |
| Skupina DPH zboží | ITMCostTrans.TaxItemGroup | Nvarchar(10) | Číslo | Číslo |
| Úprava hodnoty | ITMCostTrans.ValueAdjustmentMethod | Int | Číslo | Číslo |

### <a name="transaction-table"></a>Tabulka transakcí

Záznam nákladové transakce je spojen s nákladovou oblastí prostřednictvím přiřazení čísla tabulky transakcí (`TransTableId`). Když jsou vyžadována specifická identifikační čísla tabulek, entity jsou rozděleny na základě těchto hodnot, takže pro každou nákladovou oblast existuje entita.

Hodnota pro tabulku transakcí (`TransTableId`) je implicitní při výběru entity nákladové transakce.

### <a name="calculated-fields"></a>Kalkulovaná pole

Následující pole nejsou k dispozici při vložení nebo aktualizaci, když je použita entita nákladové transakce, protože tato pole se nastavují pouze tehdy, když jsou proti záznamu cesty provedeny konkrétní akce:

- **Odhadované náklady** – Toto pole se nastavuje, když je zaúčtována faktura za plavbu (objednávka) nebo je přijat převod.
- **Měna odhadovaných nákladů** – Toto pole se nastavuje, když je zaúčtována faktura za cestu (nákupní objednávka) nebo je přijat převod.
- **Skutečné náklady** – Toto pole se nastavuje při zaúčtování faktury dodavatele. Je spojené s náklady.

### <a name="find-auto-costs"></a>Najít automatické náklady

Tlačítko **Najít automatické náklady**, které je k dispozici u každé nákladové oblasti (cesta, přepravní kontejner atd.), poskytuje způsob, jak aktualizovat nákladové transakce pro danou nákladovou oblast z informací v konfiguračních tabulkách. Když vyberete tlačítko pro nákladovou oblast, systém vymaže stávající náklady pro tuto nákladovou oblast a vytvoří nové záznamy na základě aktuální konfigurace tabulek automatického nastavení nákladů.

Záznamy nákladových transakcí, které jsou vytvořeny pomocí datové entity, jsou označeny jako importované. Tyto záznamy se neodstraní, když vyberete možnost **Najít automatické náklady**, protože nebudou znovu vytvořeny z tabulek automatického nastavení nákladů. Záznam nákladové transakce, který je označen jako importovaný, však lze stále odstranit.

### <a name="linked-fields"></a>Propojená pole

Každá nákladová transakce může být spojena s jiným záznamem ve stejné nákladové oblasti. Tato asociace vzniká prostřednictvím pole **Propojený typ nákladů**. Umožňuje vypočítat hodnotu nákladů jako procento jiných nákladů.

Pole **Propojený typ nákladů** lze ověřit pouze v případě, že záznam, na který se odkazuje, je zpracován jako první nebo pokud již v tabulce existuje. Stejný požadavek platí pro pole **Propojený úsek**, které se používá pouze pro náklady v nákladové oblasti přepravního kontejneru.
