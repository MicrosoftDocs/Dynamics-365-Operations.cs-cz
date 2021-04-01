---
title: Konfigurace DPH pro online objednávky
description: Tohle téma poskytuje přehled o výběru skupiny DPH pro různé typy online objednávek v Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254834"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigurace DPH pro online objednávky

[!include [banner](includes/banner.md)]

Tohle téma poskytuje přehled o výběru skupiny DPH pro různé typy online objednávek. 

Pro svůj kanál elektronického obchodování možná bude chtít podporu možností, jako je doručení nebo vyzvednutí online objednávek. Uplatnění DPH závisí na možnosti vybrané vašimi online uživateli. Když se zákazník webu rozhodne koupit položku online a odešle ji na adresu, DPH se určí na základě nastavení daňové skupiny pro dodací adresu zákazníka. Když se zákazník rozhodne vyzvednout si zakoupenou položku v obchodě, DPH se určí na základě nastavení daňové skupiny obchodu pro vyzvednutí. 

## <a name="orders-shipped-to-a-customer-address"></a>Objednávky odeslané na adresu zákazníka 

Obecně jsou daně u online objednávek, které jsou dodávány na adresy zákazníků, definovány podle cílového místa. Každá skupina DPH má konfiguraci daně na základě cílového místa maloobchodu, ve které může vaše firma v hierarchické podobě definovat podrobnosti o cílovém místě, jako je kraj/oblast, stát, kraj a město. Když je zadána online objednávka, daňový modul Commerce použije dodací adresu každé řádkové položky v objednávce a vyhledá skupiny DPH s odpovídajícími cílovými daňovými kritérii. Například u online objednávky s dodací adresou řádkové položky do San Franciska v Kalifornii vyhledá daňový modul skupinu DPH a kód DPH pro Kalifornii a poté odpovídajícím způsobem vypočítá daň pro každou řádkovou položku.  

## <a name="customer-based-tax-groups"></a>Zákaznické daňové skupiny

V centrále Commerce existují dvě místa, kde jsou nakonfigurovány daňové skupiny pro zákazníky:

- **Profil zákazníka**
- **Dodací adresa zákazníka**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Když má profil zákazníka nakonfigurovanou daňovou skupinu

Záznam profilu zákazníka v centrále může mít nakonfigurovanou skupinu DPH, ale u online objednávek nebude skupinu DPH nakonfigurovanou v profilu zákazníka daňový modul používat. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Když má dodací adresa zákazníka nakonfigurovanou daňovou skupinu

Pokud má záznam dodací adresy zákazníka nakonfigurovanou daňovou skupinu a online objednávka (nebo řádková položka) je odeslána na dodací adresu zákazníka, daňová skupina nakonfigurovaná v záznamu adresy zákazníka bude použita daňovým modulem pro výpočet daně.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Konfigurace daňové skupiny pro záznam dodací adresy zákazníka

Chcete-li nakonfigurovat daňovou skupinu pro záznam dodací adresy zákazníka v centrále Commerce, postupujte takto.

1. Jděte na **Všichni zákazníci** a poté vyberte požadovaného zákazníka. 
1. Na záložce s náhledem **Adresy** vyberte požadovanou adresu a poté vyberte **Další možnosti \> Rozšířené**. 
1. Na kartě **Obecné** na stránce **Spravovat adresy** podle potřeby nastavte hodnotu DPH.

> [!NOTE]
> Daňová skupina je definována pomocí doručovací adresy řádku objednávky a daně založené na cílovém umístění se konfigurují u samotné daňové skupiny. Další informace viz [Nastavení daní pro online obchody podle cílového místa](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Vyzvednutí objednávky v obchodě

U řádků objednávky se zadaným vyzvednutím v obchodě nebo pouličním výdejem se použije daňová skupina z vybraného obchodu pro vyzvednutí. Podrobnosti, jak konfigurovat daňovou skupinu pro daný obchod, viz [Nastavení dalších daňových možností pro obchody](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Když je řádek objednávky vyzvednut v obchodě, daňový modul bude ignorovat nastavení daně z adresy zákazníka (pokud je nastaveno) a použije se konfigurace daně obchodu pro vyzvednutí. 

## <a name="additional-resources"></a>Další prostředky

[Přehled DPH](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Metody výpočtu DPH v poli Zdroj](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ Přiřazení a přepsání DPH](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Možnosti výpočtu celé částky a intervalu pro kódy daně z prodeje](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Výpočet osvobození od daně](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]